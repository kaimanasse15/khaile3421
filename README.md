
import com.sun.source.tree.ClassTree;
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;


// frame

public class StudentManager implements StudentManagerInterface{
    public class StudentManager extends JFrame{
        public StudentManager(){
        setTitle("Student Review");
        setSize(500, 600);
        setResizable(false);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        Dimension screenSize = getToolkit().getScreenSize();
        setLocation((screenSize.width - getWidth())/2,(screenSize.height - getHeight()) /2);

        //test
        JPanel supPanel = new JPanel();
        getContentPane().add(supPanel);
        supPanel.setLayout(null);

        Label idLabel = new Label("ID");
        idLabel.setBounds(40,200,30,30);
        supPanel.add(idLabel);

        JTextField idField = new JTextField();
        idField.setBounds(100,200,100,30);
        supPanel.add(idField);

        Label LastLabel = new Label("Last");
        LastLabel.setBounds(40,250,30,30);
        supPanel.add(LastLabel);

        JTextField LastField = new JTextField();
        LastField.setBounds(100,250,100,35);
        supPanel.add(LastField);

        Label FirstLabel = new Label("First");
        FirstLabel.setBounds(40,300,30,30);
        supPanel.add(FirstLabel);
// test the box
        JTextField FirstField = new JTextField();
        FirstField.setBounds(100,300,100,35);
        supPanel.add(FirstField);

        Label EmailLabel = new Label("Email");
        EmailLabel.setBounds(40,350,30,30);
        supPanel.add(EmailLabel);
// test the box
        JTextField EmailField = new JTextField();
        EmailField.setBounds(100,350,100,35);
        supPanel.add(EmailField);

        Label PhoneLabel = new Label("Phone");
        PhoneLabel.setBounds(40,400,30,30);
        supPanel.add(PhoneLabel);
// test the box
        JTextField PhoneField = new JTextField();
        PhoneField.setBounds(100,400,100,35);
        supPanel.add(PhoneField);

        JButton previousButton = new JButton("Prev");
        previousButton.setBounds(250,0,100,30);
        supPanel.add(previousButton);

        JButton NextButton = new JButton("Next");
        NextButton.setBounds(370,0,100,30);
        supPanel.add(NextButton);

        JButton LoadButton = new JButton("Load Data");
        LoadButton.setBounds(40,0,100,30);
        supPanel.add(LoadButton);
        NextButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                idField.setText("");
                LastField.setText("");
                FirstField.setText("");
                EmailField.setText("");
                PhoneField.setText("");
            }
        });


        //** JLabel idLabel = new JLabel("Name");
        //**  idLabel.setBounds(25,25,100,30);
        //** mainPanel.add(idLabel);


        setVisible(true);

        // create a new frame

    }
    // private class tryMeListener implements ActionListenner {
    // @override
    //public void actionPerformed(ActionEvent e){
    public void main(String[] args) {
        new StudentManager();

    }
    }

    /**
     * Retrieves the count of courses
     *
     * @return count of courses
     */
    @Override
    public int getCourseCount() {
        return 0;
    }

    /**
     * Retrieves the number of students in the specified course (by index)
     *
     * @param courseIndex the index of the course
     * @return student count in that course
     */
    @Override
    public int getStudentCount(int courseIndex) {

        return 0;
    }

    /**
     * Retrieves the number of students in all courses
     *
     * @return student count in all courses
     */
    @Override
    public int getStudentCount() {
        return 0;
    }

    /**
     * Retrieves the number of students in the specified course (by name)
     *
     * @param courseName the name of the course to search for
     * @return student count in that course, or -1 if course is not found
     */
    @Override
    public int getStudentCount(String courseName) {
        return 0;
    }

    /**
     * Retrieves the course name at the specified index
     *
     * @param courseIndex index of the desired course
     * @return course name
     */
    @Override
    public String getCourseName(int courseIndex) {
        return null;
    }

    /**
     * Retrieves the student at the specifiec course and student index
     *
     * @param courseIndex  course index
     * @param studentIndex student index
     * @return student at that array position
     */
    @Override
    public Student getStudent(int courseIndex, int studentIndex) {
        return null;
    }

    /**
     * Retrieves a copy of the student array for the course at the specified index
     *
     * @param courseIndex course index
     * @return copy of student array (not a reference to the internal one)
     */
    @Override
    public Student[] getStudents(int courseIndex) {
        return new Student[0];
    }

    /**
     * Retrieves the first course index associated with the specified student id
     *
     * @param id the student id to search for
     * @return the first course index containing the specified student, or -1 if not found
     */
    @Override
    public int findStudentCourse(String id) {
        return 0;
    }
}

