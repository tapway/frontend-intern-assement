# Angular Frontend Intern Code Assessment

## Task: Create a Simple User Management Dashboard

Create a basic dashboard using Angular Material and SCSS that allows managing a list of users.

### Required Setup
```bash
ng new user-dashboard
cd user-dashboard
ng add @angular/material
```

### Requirements

1. **Navigation Bar**
- Create a simple Material toolbar with:
  - Application title "User Dashboard"
  - Theme toggle button (light/dark mode)

2. **User List**
- Implement a Material table showing users with the following columns:
  - Name
  - Email
  - Role (Admin/User)
  - Actions (Edit/Delete buttons)
- Add a "Add User" button above the table

3. **User Form**
- Create a dialog form for adding/editing users with:
  - Name input (required)
  - Email input (required, with email validation)
  - Role select (Admin/User)
  - Save & Cancel buttons

### Sample Interface
```typescript
interface User {
  id: number;
  name: string;
  email: string;
  role: 'Admin' | 'User';
}

// Sample data
const SAMPLE_USERS: User[] = [
  {
    id: 1,
    name: 'John Doe',
    email: 'john@example.com',
    role: 'Admin'
  },
  {
    id: 2,
    name: 'Jane Smith',
    email: 'jane@example.com',
    role: 'User'
  }
];
```

### Sample Required Material Modules
```typescript
import { MatToolbarModule } from '@angular/material/toolbar';
import { MatTableModule } from '@angular/material/table';
import { MatButtonModule } from '@angular/material/button';
import { MatDialogModule } from '@angular/material/dialog';
import { MatFormFieldModule } from '@angular/material/form-field';
import { MatInputModule } from '@angular/material/input';
import { MatSelectModule } from '@angular/material/select';
import { MatIconModule } from '@angular/material/icon';
```

### SCSS Requirements
1. Use variables for colors and spacing
2. Make the table responsive
3. Style the form fields consistently

Example SCSS structure:
```scss
// styles/_variables.scss
$primary-color: #3f51b5;
$spacing: (
  small: 8px,
  medium: 16px,
  large: 24px
);

// Component styles
.user-dashboard {
  padding: map-get($spacing, medium);
  
  &__header {
    margin-bottom: map-get($spacing, large);
  }
  
  &__table {
    width: 100%;
    overflow-x: auto;
  }
}
```

### Evaluation Criteria (100 points)

1. **Basic Requirements (40 points)**
- Functioning navigation bar (10 points)
- Complete user table display (15 points)
- Working add/edit form (15 points)

2. **Angular Material Usage (30 points)**
- Proper component implementation (15 points)
- Theme implementation (15 points)

3. **SCSS & Styling (20 points)**
- Use of variables and proper organization (10 points)
- Responsive design (10 points)

4. **Code Quality (10 points)**
- Clean, readable code
- Proper TypeScript usage
- Component organization

### Bonus Points (20 extra points)
- Implementing form validation messages
- Adding loading states
- Adding sorting to the table
- Adding simple animations

### Submission Instructions
1. Create a new GitHub repository
2. Push your code
3. Include a README with:
   - Setup instructions
   - Features implemented
   - Any additional notes

### Tips for Candidates
- Focus on completing the basic requirements first
- Keep the code clean and well-organized
- Comment your code where necessary
- Test your application's responsiveness
