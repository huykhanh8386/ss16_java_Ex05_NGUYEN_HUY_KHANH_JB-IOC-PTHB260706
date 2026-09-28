package Ex05;

import java.util.List;
import java.util.stream.Collectors;

public class DepartmentService {

    public static List<String> getEmployeeNamesByDept(
            List<Employee> list,
            String dept) {
        return list.stream()
                .filter(e -> e.getDepartment().equalsIgnoreCase(dept))
                .map(Employee::getName)
                .map(String::toUpperCase)
                .collect(Collectors.toList());
    }
}
