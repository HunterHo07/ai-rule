# AI Rules System

1. Memory Management
   - Dynamic memory allocation that adapts to needs
   - Smart caching with predictive loading
   - Full context retention with instant access
   - Parallel processing capabilities
   - No artificial memory limits

2. Security Framework
   - Command validation required
   - Package verification required
   - Token validation required
   - Active monitoring enabled
   - Real-time security alerts

3. Processing Framework
   - Parallel processing enabled
   - Asynchronous operations supported
   - Smart batch processing
   - Adaptive optimization strategy
   - Predictive caching

4. AI Capabilities
   - Code Understanding:
     * Semantic analysis
     * Context awareness
     * Pattern recognition
     * Dependency tracking
     * Code flow analysis
     * Impact assessment

   - Learning System:
     * Adaptive responses
     * Style matching
     * Context learning
     * Pattern recognition
     * Workflow optimization

   - Assistance Modes:
     * Proactive suggestions
     * Error prevention
     * Reactive support
     * Collaborative coding

5. Error Handling
   - Prevention:
     * Static analysis
     * Runtime prediction
     * Context validation
   
   - Recovery:
     * Auto-correction
     * Smart suggestions
     * Alternative solutions

6. Code Quality
   - Analysis:
     * Complexity checking
     * Maintainability review
     * Reliability assessment
   
   - Standards:
     * Best practices enforcement
     * Pattern recognition
     * Anti-pattern detection

7. Interaction
   - Clear communication
   - Context adaptation
   - Skill-level matching
   - Knowledge sharing
   - Pair programming support

8. System Integration
   - IDE feature support
   - External tool integration
   - Workflow automation
   - Continuous improvement

9. File Type Usage
   - Use .md files for human reading
   - Use .rule files for AI processing
   - Keep both formats in sync

10. AI Startup Process
    - Check .ai folder first
    - Load all .rules files
    - Ignore non-rule files except TODO
    - Process in order:
      1. Load .rules
      2. Check TODO.rules
      3. Reference TODO.md

11. TODO Management
    - TODO.md:
      * Human-readable task list
      * Progress tracking
      * Task status updates
      * Completion history
    
    - TODO.rules:
      * AI-processable tasks
      * Only contains active tasks
      * Remove completed tasks
      * Auto-update with TODO.md

12. Task Synchronization
    - Update TODO.md when tasks complete
    - Remove done tasks from TODO.rules
    - Keep only active tasks in .rules
    - Maintain task history in .md

13. Token Counting Rules (Corrected)
    - Words are split into subwords/tokens regardless of case:
      * "ProgressTracking" = 2 tokens (Progress + Tracking)
      * "progress_tracking" = 2 tokens (progress + tracking)
      * "progresstracking" = 2 tokens (progress + tracking)
    
    - Common splits:
      * Capital letters often indicate splits
      * Underscores cause splits
      * Numbers are usually separate tokens
      * Special characters are separate tokens
    
    - Examples:
      * "ThisIs" = 2 tokens (This + Is)
      * "this_is" = 2 tokens (this + is)
      * "Rule123" = 2 tokens (Rule + 123)
      * "AI" = 1 token
      * "GPT3" = 2 tokens (GPT + 3)
    
    - Long words example:
      * "ThisIsRuleThatMustFollowButHowManyTokenThisWordCountInAi"
      * Actually splits into ~15 tokens:
        - This, Is, Rule, That, Must, Follow, But, How, Many
        - Token, This, Word, Count, In, Ai

14. Token Best Practices
    - Case style doesn't affect token count
    - Word choice matters more than formatting
    - Common words often count as single tokens
    - Technical terms may split into multiple tokens
    - Numbers and special chars are usually separate tokens

15. Information Verification Rules
    - Triple Verification Required:
      * First Check: Initial research/knowledge
      * Second Check: Cross-reference with reliable sources
      * Third Check: Test with examples
      * Final: Only proceed if all checks pass
    
    - Confirmation Process:
      * Research multiple sources
      * Test with different examples
      * Verify edge cases
      * Document verification steps
      * Note any uncertainties
    
    - Before Output:
      * Verify all information is current
      * Check for contradictions
      * Test critical examples
      * Note confidence level
      * Mark unverified information
    
    - When Uncertain:
      * State uncertainty clearly
      * Provide confidence level
      * Show verification attempts
      * Request additional verification
      * Defer to authoritative sources

16. MD-RULE Sync Rules
    - File Pairing:
      * Every .md must have matching .rule
      * Matching files must stay synchronized
      * Changes in one require update in other
      * Sync check before any modifications
    
    - Sync Verification:
      * Check section count matches
      * Verify all rules are represented
      * Compare content structure
      * Validate rule mappings
      * Track last sync time
    
    - Update Process:
      * Update both files together
      * Never update one without other
      * Verify sync after updates
      * Log sync status
      * Mark sync timestamp
    
    - Sync Status:
      * Track in both files
      * Include last sync time
      * Mark unsynced sections
      * Flag sync conflicts
      * Required sync checks

17. Advanced Sync Verification
    - Structure Checks:
      * Compare section hierarchies
        → Maps to structure_checks.compare_hierarchies
        → Includes full depth tree comparison
        → Tracks all changes and comments
      
      * Validate rule relationships
        → Maps to structure_checks.validate_relationships
        → Checks parent/child/sibling relations
        → Detects circular dependencies
      
      * Check cross-references
        → Maps to structure_checks.cross_references
        → Bidirectional link verification
        → Automatic repair of broken links
      
      * Verify rule dependencies
        → Maps to structure_checks.rule_dependencies
        → Cascade updates through chain
        → Prevents dependency conflicts
      
      * Match rule priorities
        → Maps to structure_checks.rule_priorities
        → Enforces priority inheritance
        → Handles override rules
    
    - Content Validation:
      * Deep content comparison
        → Maps to content_validation.deep_comparison
        → Compares text, structure, metadata
        → Case-sensitive with whitespace handling
      
      * Semantic equivalence check
        → Maps to content_validation.semantic_equivalence
        → Uses NLP for context awareness
        → 95% threshold for matching
      
      * Format consistency check
        → Maps to content_validation.format_consistency
        → Supports md/rule/json formats
        → Automatic formatting
      
      * Version alignment
        → Maps to content_validation.version_alignment
        → Uses semantic versioning
        → Maintains changelog
      
      * Metadata verification
        → Maps to content_validation.metadata_verification
        → Required fields: timestamp, author, version
        → Automatic updates for missing data
    
    - Integrity Checks:
      * Hash comparison
        → Maps to integrity_checks.hash_comparison
        → Uses SHA256 algorithm
        → Stores historical hashes
      
      * Checksum validation
        → Maps to integrity_checks.checksum_validation
        → Uses MD5 for quick checks
        → Real-time verification
      
      * Structure integrity
        → Maps to integrity_checks.structure_integrity
        → Validates syntax and schema
        → Safe auto-fix capability
      
      * Reference integrity
        → Maps to integrity_checks.reference_integrity
        → Fixes broken references
        → Maintains reference history
      
      * Dependency chain check
        → Maps to integrity_checks.dependency_chain
        → Checks up to 50 levels deep
        → Caches results for performance

18. Sync Conflict Resolution
    - Conflict Types:
      * Content mismatch
      * Structure difference
      * Version conflict
      * Timestamp mismatch
      * Rule inconsistency
    
    - Resolution Steps:
      * Identify conflict source
      * Compare versions
      * Merge changes safely
      * Validate merged state
      * Update both files
    
    - Conflict Prevention:
      * Lock files during updates
      * Version control
      * Change tracking
      * Backup before changes
      * Atomic updates

19. Automated Sync Procedures
    - Auto-Check Triggers:
      * Before file load
      * After file save
      * Before rule application
      * After content update
      * On version change
    
    - Automated Tasks:
      * Regular sync checks
      * Backup creation
      * Conflict detection
      * Version tracking
      * Health monitoring
    
    - Recovery Procedures:
      * Auto-backup restore
      * Version rollback
      * Conflict auto-resolve
      * Integrity repair
      * Sync state reset

20. Testing Rules and Requirements

## Coverage Requirements
- 100% test coverage mandatory for all components
- Includes unit tests, integration tests, security tests, and e2e tests
- Automated coverage reporting and verification

## Security Testing
### Input Validation
- SQL injection prevention
- XSS attack protection
- Command injection checks
- Path traversal prevention
- Special character handling

### Authentication & Authorization
- Token validation
- Session management
- Password policy enforcement
- 2FA verification
- Role-based access control
- Resource permission validation
- API endpoint security
- Data access controls

### Data Protection
- Encryption standards
- Input/Output sanitization
- Secure storage practices
- Secure data transmission

## Component-Specific Testing

### Frontend Testing
- Component testing
- UI security validation
- CSRF protection
- Input validation
- Cross-browser security
- Client-side security

### Backend Testing
- API security testing
- Data validation
- Rate limiting
- Authentication flows
- Authorization checks
- Error handling security

### Database Testing
- Query injection prevention
- Access control validation
- Data integrity checks
- Backup/recovery testing
- Schema security

### Infrastructure Testing
- Network security
- Server hardening
- SSL/TLS configuration
- Firewall rule validation
- Security patch testing

## Test Structure Creation
Test directories are automatically created when development components are detected:

### Frontend Detection
```
/tests/frontend/
  ├── unit/
  ├── integration/
  ├── e2e/
  └── security/
```

### Backend Detection
```
/tests/backend/
  ├── unit/
  ├── integration/
  ├── security/
  └── performance/
```

### Database Detection
```
/tests/db/
  ├── queries/
  ├── migrations/
  └── security/
```

## Implementation Notes
- Test folders are created only when corresponding development is detected
- All security checks are mandatory before deployment
- Continuous testing during development
- Automated security scanning integration

## Security Best Practices
- Regular security audits
- Dependency vulnerability scanning
- Security patch management
- Access control reviews
- Penetration testing requirements

## Tech Stack Integration
- Rules Location: TECH_STACK.rule
- AI Reading:
  - Enabled with high priority
  - Automatic updates
  - Validation enabled
- Rule Linking:
  - Cross-referencing enabled
  - Conflict resolution
- File Types: .rule, .md

## Code Improvement Detection
- Automatic code scanning on changes
- Aspects checked:
  - Performance
  - Security
  - Maintainability
  - DRY principles
  - Outdated technology
- Required TODO tags with:
  - Reason for improvement
  - Timestamp
  - Detailed explanation

## Tech Stack Monitoring
- Daily checks at 00:00
- Monitors:
  - Framework updates
  - Security patches
  - New features
  - Deprecation notices
- Automatic notifications

## Breaking Changes
- Pre-task project checks:
  - Dependencies
  - API compatibility
  - Database schema
  - File structure
- Commit warnings required for:
  - Schema changes
  - API changes
  - Dependency updates
  - Security patches
- Confirmation required for breaking changes

file:end
