# Engineering Manager Dashboard

A web application designed to help software engineering managers efficiently handle their daily responsibilities through clear, text-based workflows and actionable task management.

## Purpose

This application addresses the core challenge engineering managers face: coordinating multiple teams, tracking individual contributors, and maintaining clear communication across projects without getting overwhelmed by information overload.

## Design Philosophy

**Aphantasia-Friendly Design**: This application prioritizes text-based, concrete information over visual metaphors. Features are described through their actions and outcomes, with clear labeling and explicit state indicators rather than colors, icons, or visual representations alone.

## Core Features

### Team Management
- **Team Roster**: Maintain an up-to-date list of team members with their roles, current assignments, and contact information
- **Availability Tracking**: Record team members' working hours, time off, and current capacity
- **Skill Inventory**: Document each team member's technical skills, experience levels, and areas of expertise

### Task & Project Coordination
- **Assignment Tracking**: View all current assignments with explicit status labels (e.g., "Not Started", "In Progress", "Blocked", "Complete")
- **Workload Distribution**: See numerical indicators of each team member's current task count and estimated hours
- **Dependency Mapping**: List tasks with their blockers and dependencies in plain text format
- **Priority Queue**: Order tasks by explicit priority levels (Critical, High, Normal, Low)

### Communication Hub
- **One-on-One Schedule**: Track scheduled and completed one-on-one meetings with notes and action items
- **Meeting Preparation**: Maintain agendas with specific discussion points and outcomes
- **Feedback Log**: Record feedback given to team members with dates and context
- **Follow-up Items**: Track commitments made during conversations with completion status

### Performance & Growth
- **Goal Tracking**: Document individual and team goals with measurable success criteria
- **Progress Checkpoints**: Record milestone completions and review dates
- **Growth Plans**: Maintain development plans with specific learning objectives and resources
- **Achievement Log**: Document completed projects, solved problems, and notable contributions

### Daily Workflow Tools
- **Daily Standup Prep**: Generate summaries of yesterday's completions, today's plans, and current blockers
- **Escalation Tracker**: Monitor issues requiring manager intervention with status and resolution notes
- **Decision Log**: Record decisions made, rationale, and stakeholders informed
- **Action Items**: Centralized list of manager tasks with due dates and completion status

## Key Benefits

1. **Reduced Context Switching**: All manager responsibilities accessible from a single interface
2. **Clear Status Indicators**: Explicit text labels eliminate ambiguity about project states
3. **Searchable History**: Find past decisions, feedback, and conversations through text search
4. **Capacity Planning**: Numerical workload data helps with assignment decisions
5. **Accountability**: Time-stamped logs of actions, decisions, and commitments

## User Workflow Example

**Morning Routine**:
1. Review overnight updates: Check tasks marked as "Blocked" or "Needs Manager Input"
2. Prepare for standup: Generate summary showing each team member's current work
3. Check calendar: View today's one-on-ones with prepared agendas and previous notes
4. Review action items: See personal tasks due today with priority indicators

**During One-on-One**:
1. Access meeting note template with agenda items
2. Review team member's current assignments and recent completions
3. Document feedback and commitments with timestamps
4. Create follow-up action items linked to this meeting

**End of Day**:
1. Update task statuses based on standup and conversations
2. Log decisions made throughout the day
3. Plan tomorrow's priorities
4. Review blocked items for next-day resolution

## Technical Stack

- **Frontend**: React with TypeScript for type safety and explicit interfaces
- **State Management**: Redux for predictable state updates
- **Data Storage**: PostgreSQL for structured, queryable data
- **API**: RESTful endpoints with clear request/response contracts
- **Authentication**: OAuth 2.0 for secure access control

## Getting Started

### Prerequisites
- Node.js (version 18 or higher)
- PostgreSQL (version 14 or higher)
- npm or yarn package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/andres-fu/dw_ce_fuentes_01202021.git

# Navigate to project directory
cd dw_ce_fuentes_01202021

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your database credentials and API keys

# Run database migrations
npm run migrate

# Start development server
npm run dev
```

### Configuration

Edit `.env` file with the following required variables:
- `DATABASE_URL`: PostgreSQL connection string
- `SESSION_SECRET`: Random string for session management
- `PORT`: Application port (default: 3000)

## Data Management

### Backup
All data is stored in PostgreSQL with daily automated backups. Export functionality allows downloading team data in JSON or CSV formats.

### Privacy
- Team member data is encrypted at rest
- Access logs track who viewed or modified information
- Data retention policies can be configured per organization

## Usage Guide

### Adding a Team Member
1. Navigate to "Team" section
2. Click "Add Team Member" button
3. Enter required fields: Name, Email, Role, Start Date
4. Add optional fields: Skills, Working Hours, Location
5. Click "Save" - confirmation message appears with member's name

### Creating a Task Assignment
1. Navigate to "Tasks" section
2. Click "New Assignment" button
3. Select team member from dropdown list
4. Enter task description, estimated hours, and due date
5. Set priority level: Critical, High, Normal, or Low
6. Add dependencies if applicable
7. Click "Create" - task appears in member's assignment list

### Preparing for One-on-One
1. Navigate to "One-on-Ones" section
2. Select upcoming meeting from list
3. Review auto-generated summary: recent tasks, feedback history, goals progress
4. Add agenda items as bullet points
5. During meeting, take notes in provided text area
6. Mark action items with checkbox format
7. Click "Complete Meeting" to archive notes and create follow-ups

## Accessibility Features

- **High Contrast Mode**: Enhanced text contrast for readability
- **Keyboard Navigation**: All features accessible via keyboard shortcuts
- **Screen Reader Compatible**: Semantic HTML with ARIA labels
- **Text-Only Mode**: Option to disable all visual decorations
- **Customizable Labels**: Rename feature sections to match your terminology

## Contributing

We welcome contributions that maintain the application's focus on clear, text-based functionality.

### Contribution Guidelines
1. Ensure new features have explicit text labels for all states
2. Avoid relying solely on visual indicators (colors, icons, positions)
3. Provide keyboard shortcuts for new functionality
4. Include plain-text descriptions for all UI elements
5. Write tests covering the functional behavior

### Development Workflow
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make changes with clear commit messages
4. Run tests: `npm test`
5. Submit pull request with description of functionality added

## Support

For questions, bug reports, or feature requests:
- Create an issue in the GitHub repository
- Tag with appropriate label: bug, enhancement, question
- Provide specific steps to reproduce any issues

## License

MIT License - See LICENSE file for details

## Roadmap

**Planned Features**:
- Integration with project management tools (Jira, Linear)
- Slack integration for status updates
- Report generation for skip-level meetings
- Team capacity forecasting
- Anonymous feedback collection
- Mobile-responsive interface

**Current Version**: 0.1.0-alpha
**Status**: Active development
