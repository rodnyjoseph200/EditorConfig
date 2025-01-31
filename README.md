# .NET EditorConfig

<details>

<summary> ## Table of Content </summary>

- [1. indent_size](#1-indent_size)
- [2. indent_style](#2-indent_style)
- [3. tab_width](#3-tab_width)
- [4. end_of_line](#4-end_of_line)
- [5. insert_final_newline](#5-insert_final_newline)
- [6. dotnet_separate_import_directive_groups](#6-dotnet_separate_import_directive_groups)
- [7. dotnet_sort_system_directives_first](#7-dotnet_sort_system_directives_first)
- [8. file_header_template](#8-file_header_template)
- [9. dotnet_style_qualification_for_event](#9-dotnet_style_qualification_for_event)
- [10. dotnet_style_qualification_for_field](#10-dotnet_style_qualification_for_field)
- [11. dotnet_style_qualification_for_method](#11-dotnet_style_qualification_for_method)
- [12. dotnet_style_qualification_for_property](#12-dotnet_style_qualification_for_property)
- [13. dotnet_style_predefined_type_for_locals_parameters_members](#13-dotnet_style_predefined_type_for_locals_parameters_members)
- [14. dotnet_style_predefined_type_for_member_access](#14-dotnet_style_predefined_type_for_member_access)
- [15. dotnet_style_parentheses_in_arithmetic_binary_operators](#15-dotnet_style_parentheses_in_arithmetic_binary_operators)
- [16. dotnet_style_parentheses_in_other_binary_operators](#16-dotnet_style_parentheses_in_other_binary_operators)
- [17. dotnet_style_parentheses_in_other_operators](#17-dotnet_style_parentheses_in_other_operators)
- [18. dotnet_style_parentheses_in_relational_binary_operators](#18-dotnet_style_parentheses_in_relational_binary_operators)
- [19. dotnet_style_require_accessibility_modifiers](#19-dotnet_style_require_accessibility_modifiers)
- [20. dotnet_style_coalesce_expression](#20-dotnet_style_coalesce_expression)
- [21. dotnet_style_collection_initializer](#21-dotnet_style_collection_initializer)
- [22. dotnet_style_explicit_tuple_names](#22-dotnet_style_explicit_tuple_names)
- [23. dotnet_style_namespace_match_folder](#23-dotnet_style_namespace_match_folder)
- [24. dotnet_style_null_propagation](#24-dotnet_style_null_propagation)
- [25. dotnet_style_object_initializer](#25-dotnet_style_object_initializer)
- [26. dotnet_style_operator_placement_when_wrapping](#26-dotnet_style_operator_placement_when_wrapping)
- [27. dotnet_style_prefer_auto_properties](#27-dotnet_style_prefer_auto_properties)
- [28. dotnet_style_prefer_collection_expression](#28-dotnet_style_prefer_collection_expression)
- [29. dotnet_style_prefer_compound_assignment](#29-dotnet_style_prefer_compound_assignment)
- [30. dotnet_style_prefer_conditional_expression_over_assignment](#30-dotnet_style_prefer_conditional_expression_over_assignment)
- [31. dotnet_style_prefer_conditional_expression_over_return](#31-dotnet_style_prefer_conditional_expression_over_return)
- [32. dotnet_style_prefer_foreach_explicit_cast_in_source](#32-dotnet_style_prefer_foreach_explicit_cast_in_source)
- [33. dotnet_style_prefer_inferred_anonymous_type_member_names](#33-dotnet_style_prefer_inferred_anonymous_type_member_names)
- [34. dotnet_style_prefer_inferred_tuple_names](#34-dotnet_style_prefer_inferred_tuple_names)
- [35. dotnet_style_prefer_is_null_check_over_reference_equality_method](#35-dotnet_style_prefer_is_null_check_over_reference_equality_method)
- [36. dotnet_style_prefer_simplified_boolean_expressions](#36-dotnet_style_prefer_simplified_boolean_expressions)
- [37. dotnet_style_prefer_simplified_interpolation](#37-dotnet_style_prefer_simplified_interpolation)
- [38. dotnet_style_readonly_field](#38-dotnet_style_readonly_field)
- [39. dotnet_code_quality_unused_parameters](#39-dotnet_code_quality_unused_parameters)
- [40. dotnet_remove_unnecessary_suppression_exclusions](#40-dotnet_remove_unnecessary_suppression_exclusions)
- [41. dotnet_style_allow_multiple_blank_lines_experimental](#41-dotnet_style_allow_multiple_blank_lines_experimental)
- [42. dotnet_style_allow_statement_immediately_after_block_experimental](#42-dotnet_style_allow_statement_immediately_after_block_experimental)
- [43. csharp_style_var_elsewhere](#43-csharp_style_var_elsewhere)
- [44. csharp_style_var_for_built_in_types](#44-csharp_style_var_for_built_in_types)
- [45. csharp_style_var_when_type_is_apparent](#45-csharp_style_var_when_type_is_apparent)
- [46. csharp_style_expression_bodied_accessors](#46-csharp_style_expression_bodied_accessors)
- [47. csharp_style_expression_bodied_constructors](#47-csharp_style_expression_bodied_constructors)
- [48. csharp_style_expression_bodied_indexers](#48-csharp_style_expression_bodied_indexers)
- [49. csharp_style_expression_bodied_lambdas](#49-csharp_style_expression_bodied_lambdas)
- [50. csharp_style_expression_bodied_local_functions](#50-csharp_style_expression_bodied_local_functions)
- [51. csharp_style_expression_bodied_methods](#51-csharp_style_expression_bodied_methods)
- [52. csharp_style_expression_bodied_operators](#52-csharp_style_expression_bodied_operators)
- [53. csharp_style_expression_bodied_properties](#53-csharp_style_expression_bodied_properties)
- [54. csharp_style_pattern_matching_over_as_with_null_check](#54-csharp_style_pattern_matching_over_as_with_null_check)
- [55. csharp_style_pattern_matching_over_is_with_cast_check](#55-csharp_style_pattern_matching_over_is_with_cast_check)
- [56. csharp_style_prefer_extended_property_pattern](#56-csharp_style_prefer_extended_property_pattern)
- [57. csharp_style_prefer_not_pattern](#57-csharp_style_prefer_not_pattern)
- [58. csharp_style_prefer_pattern_matching](#58-csharp_style_prefer_pattern_matching)
- [59. csharp_style_prefer_switch_expression](#59-csharp_style_prefer_switch_expression)
- [60. csharp_style_conditional_delegate_call](#60-csharp_style_conditional_delegate_call)
- [61. csharp_prefer_static_anonymous_function](#61-csharp_prefer_static_anonymous_function)
- [62. csharp_prefer_static_local_function](#62-csharp_prefer_static_local_function)
- [63. csharp_preferred_modifier_order](#63-csharp_preferred_modifier_order)
- [64. csharp_style_prefer_readonly_struct](#64-csharp_style_prefer_readonly_struct)
- [65. csharp_style_prefer_readonly_struct_member](#65-csharp_style_prefer_readonly_struct_member)
- [66. csharp_prefer_braces](#66-csharp_prefer_braces)
- [67. csharp_prefer_simple_using_statement](#67-csharp_prefer_simple_using_statement)
- [68. csharp_style_namespace_declarations](#68-csharp_style_namespace_declarations)
- [69. csharp_style_prefer_method_group_conversion](#69-csharp_style_prefer_method_group_conversion)
- [70. csharp_style_prefer_primary_constructors](#70-csharp_style_prefer_primary_constructors)
- [71. csharp_style_prefer_top_level_statements](#71-csharp_style_prefer_top_level_statements)
- [72. csharp_prefer_simple_default_expression](#72-csharp_prefer_simple_default_expression)
- [73. csharp_style_deconstructed_variable_declaration](#73-csharp_style_deconstructed_variable_declaration)
- [74. csharp_style_implicit_object_creation_when_type_is_apparent](#74-csharp_style_implicit_object_creation_when_type_is_apparent)
- [75. csharp_style_inlined_variable_declaration](#75-csharp_style_inlined_variable_declaration)
- [76. csharp_style_prefer_index_operator](#76-csharp_style_prefer_index_operator)
- [77. csharp_style_prefer_local_over_anonymous_function](#77-csharp_style_prefer_local_over_anonymous_function)
- [78. csharp_style_prefer_null_check_over_type_check](#78-csharp_style_prefer_null_check_over_type_check)
- [79. csharp_style_prefer_range_operator](#79-csharp_style_prefer_range_operator)
- [80. csharp_style_prefer_tuple_swap](#80-csharp_style_prefer_tuple_swap)
- [81. csharp_style_prefer_utf8_string_literals](#81-csharp_style_prefer_utf8_string_literals)
- [82. csharp_style_throw_expression](#82-csharp_style_throw_expression)
- [83. csharp_style_unused_value_assignment_preference](#83-csharp_style_unused_value_assignment_preference)
- [84. csharp_style_unused_value_expression_statement_preference](#84-csharp_style_unused_value_expression_statement_preference)
- [85. csharp_using_directive_placement](#85-csharp_using_directive_placement)
- [86. csharp_style_allow_blank_line_after_colon_in_constructor_initializer_experimental](#86-csharp_style_allow_blank_line_after_colon_in_constructor_initializer_experimental)
- [87. csharp_style_allow_blank_line_after_token_in_arrow_expression_clause_experimental](#87-csharp_style_allow_blank_line_after_token_in_arrow_expression_clause_experimental)
- [88. csharp_style_allow_blank_line_after_token_in_conditional_expression_experimental](#88-csharp_style_allow_blank_line_after_token_in_conditional_expression_experimental)
- [89. csharp_style_allow_blank_lines_between_consecutive_braces_experimental](#89-csharp_style_allow_blank_lines_between_consecutive_braces_experimental)
- [90. csharp_style_allow_embedded_statements_on_same_line_experimental](#90-csharp_style_allow_embedded_statements_on_same_line_experimental)
- [91. csharp_new_line_before_catch](#91-csharp_new_line_before_catch)
- [92. csharp_new_line_before_else](#92-csharp_new_line_before_else)
- [93. csharp_new_line_before_finally](#93-csharp_new_line_before_finally)
- [94. csharp_new_line_before_members_in_anonymous_types](#94-csharp_new_line_before_members_in_anonymous_types)
- [95. csharp_new_line_before_members_in_object_initializers](#95-csharp_new_line_before_members_in_object_initializers)
- [96. csharp_new_line_before_open_brace](#96-csharp_new_line_before_open_brace)
- [97. csharp_new_line_between_query_expression_clauses](#97-csharp_new_line_between_query_expression_clauses)
- [98. csharp_indent_block_contents](#98-csharp_indent_block_contents)
- [99. csharp_indent_braces](#99-csharp_indent_braces)
- [100. csharp_indent_case_contents](#100-csharp_indent_case_contents)
- [101. csharp_indent_case_contents_when_block](#101-csharp_indent_case_contents_when_block)
- [102. csharp_indent_labels](#102-csharp_indent_labels)
- [103. csharp_indent_switch_labels](#103-csharp_indent_switch_labels)
- [104. csharp_space_after_cast](#104-csharp_space_after_cast)
- [105. csharp_space_after_colon_in_inheritance_clause](#105-csharp_space_after_colon_in_inheritance_clause)
- [106. csharp_space_after_comma](#106-csharp_space_after_comma)
- [107. csharp_space_after_dot](#107-csharp_space_after_dot)
- [108. csharp_space_after_keywords_in_control_flow_statements](#108-csharp_space_after_keywords_in_control_flow_statements)
- [109. csharp_space_after_semicolon_in_for_statement](#109-csharp_space_after_semicolon_in_for_statement)
- [110. csharp_space_around_binary_operators](#110-csharp_space_around_binary_operators)
- [111. csharp_space_around_declaration_statements](#111-csharp_space_around_declaration_statements)
- [112. csharp_space_before_colon_in_inheritance_clause](#112-csharp_space_before_colon_in_inheritance_clause)
- [113. csharp_space_before_comma](#113-csharp_space_before_comma)
- [114. csharp_space_before_dot](#114-csharp_space_before_dot)
- [115. csharp_space_before_open_square_brackets](#115-csharp_space_before_open_square_brackets)
- [116. csharp_space_before_semicolon_in_for_statement](#116-csharp_space_before_semicolon_in_for_statement)
- [117. csharp_space_between_empty_square_brackets](#117-csharp_space_between_empty_square_brackets)
- [118. csharp_space_between_method_call_empty_parameter_list_parentheses](#118-csharp_space_between_method_call_empty_parameter_list_parentheses)
- [119. csharp_space_between_method_call_name_and_opening_parenthesis](#119-csharp_space_between_method_call_name_and_opening_parenthesis)
- [120. csharp_space_between_method_call_parameter_list_parentheses](#120-csharp_space_between_method_call_parameter_list_parentheses)
- [121. csharp_space_between_method_declaration_empty_parameter_list_parentheses](#121-csharp_space_between_method_declaration_empty_parameter_list_parentheses)
- [122. csharp_space_between_method_declaration_name_and_open_parenthesis](#122-csharp_space_between_method_declaration_name_and_open_parenthesis)
- [123. csharp_space_between_method_declaration_parameter_list_parentheses](#123-csharp_space_between_method_declaration_parameter_list_parentheses)
- [124. csharp_space_between_parentheses](#124-csharp_space_between_parentheses)
- [125. csharp_space_between_square_brackets](#125-csharp_space_between_square_brackets)
- [126. csharp_preserve_single_line_blocks](#126-csharp_preserve_single_line_blocks)
- [127. csharp_preserve_single_line_statements](#127-csharp_preserve_single_line_statements)
- [128. dotnet_naming_rule.interface_should_be_begins_with_i](#128-dotnet_naming_ruleinterface_should_be_begins_with_i)
- [129. dotnet_naming_rule.types_should_be_pascal_case](#129-dotnet_naming_ruletypes_should_be_pascal_case)
- [130. dotnet_naming_rule.non_field_members_should_be_pascal_case](#130-dotnet_naming_rulenon_field_members_should_be_pascal_case)
- [131. trim_trailing_whitespace](#131-trim_trailing_whitespace)
- [132. dotnet_diagnostic.IDE0005.severity](#132-dotnet_diagnosticide0005severity)
- [133. dotnet_diagnostic.IDE1006.severity](#133-dotnet_diagnosticide1006severity)
- [134. dotnet_diagnostic.CS8019.severity](#134-dotnet_diagnosticcs8019severity)
- [135. dotnet_diagnostic.IDE0079.severity](#135-dotnet_diagnosticide0079severity)
- [136. dotnet_diagnostic.IDE0130.severity](#136-dotnet_diagnosticide0130severity)
- [137. dotnet_diagnostic.CS1591.severity](#137-dotnet_diagnosticcs1591severity)
- [138. csharp_prefer_system_threading_lock](#138-csharp_prefer_system_threading_lock)

</details>

---
# Rules

## 1. indent_size  
**Description**: Defines the number of spaces used for each indentation level.  

---
## 2. indent_style  
**Description**: Defines whether to use spaces or tabs for indentation.  

---
## 3. tab_width  
**Description**: Sets the number of columns used to represent a tab character if `indent_style=tab`.  

---
## 4. end_of_line  
**Description**: Sets the line ending character(s) to use (e.g., `crlf` for Windows).  

---
## 5. insert_final_newline  
**Description**: Specifies whether to ensure the file ends with a newline.  

---
## 6. dotnet_separate_import_directive_groups  
**Description**: Controls whether using directives are separated into groups by blank lines.  

---
## 7. dotnet_sort_system_directives_first  
**Description**: Enforces whether 'System' namespaces come first in usings.  

---
## 8. file_header_template  
**Description**: Controls the file header text inserted in new files.  

---
## 9. dotnet_style_qualification_for_event  
**Description**: Enforces use of `this.` qualifier for events.  
\
**Examples**  
When True  
```csharp  
this.eventHandler?.Invoke(this, EventArgs.Empty);  
```  
When False  
```csharp  
eventHandler?.Invoke(this, EventArgs.Empty);  
```  

---
## 10. dotnet_style_qualification_for_field  
**Description**: Enforces use of `this.` qualifier for fields.  
\
**Examples**  
When True  
```csharp  
this.myField = 10;  
```  
When False  
```csharp  
myField = 10;  
```  

---
## 11. dotnet_style_qualification_for_method  
**Description**: Enforces use of `this.` qualifier for methods.  
\
**Examples**  
When True  
```csharp  
this.DoSomething();  
```  
When False  
```csharp  
DoSomething();  
```  

---
## 12. dotnet_style_qualification_for_property  
**Description**: Enforces use of `this.` qualifier for properties.  
\
**Examples**  
When True  
```csharp  
this.MyProperty = 5;  
```  
When False  
```csharp  
MyProperty = 5;  
```  

---
## 13. dotnet_style_predefined_type_for_locals_parameters_members  
**Description**: Prefers language keywords (e.g., `int`) over BCL types (e.g., `Int32`).  
\
**Examples**  
When True  
```csharp  
int x = 0;  
```  
When False  
```csharp  
Int32 x = 0;  
```  

---
## 14. dotnet_style_predefined_type_for_member_access  
**Description**: Prefers language keywords when accessing static members.  
\
**Examples**  
When True  
```csharp  
string.Empty;  
```  
When False  
```csharp  
String.Empty;  
```  

---
## 15. dotnet_style_parentheses_in_arithmetic_binary_operators  
**Description**: Enforces parentheses around arithmetic expressions for clarity.  
\
**Examples**  
Option 1  
```csharp  
(a + b) * c;  
```  
Option 2  
```csharp  
a + b * c;  
```  

---
## 16. dotnet_style_parentheses_in_other_binary_operators  
**Description**: Enforces parentheses for non-arithmetic binary operators.  
\
**Examples**  
Option 1  
```csharp  
(x & y) == 0;  
```  
Option 2  
```csharp  
x & y == 0;  
```  

---
## 17. dotnet_style_parentheses_in_other_operators  
**Description**: Controls parentheses usage for cast/unary operators.  
\
**Examples**  
Option 1  
```csharp  
(int)x + 1;  
```  
Option 2  
```csharp  
(int)x + (1);  
```  

---
## 18. dotnet_style_parentheses_in_relational_binary_operators  
**Description**: Enforces parentheses around relational operators.  
\
**Examples**  
Option 1  
```csharp  
(a < b) == true;  
```  
Option 2  
```csharp  
a < b == true;  
```  

---
## 19. dotnet_style_require_accessibility_modifiers  
**Description**: Enforces accessibility keywords on members.  
\
**Examples**  
When True  
```csharp  
public void MyMethod() { }  
```  
When False  
```csharp  
void MyMethod() { }  
```  

---
## 20. dotnet_style_coalesce_expression  
**Description**: Prefers `??` operator over conditional expressions for null checks.  
\
**Examples**  
When True  
```csharp  
var result = value ?? "default";  
```  
When False  
```csharp  
var result = value != null ? value : "default";  
```  

---
## 21. dotnet_style_collection_initializer  
**Description**: Enforces using collection initializers.  
\
**Examples**  
When True  
```csharp  
var list = new List<int> { 1, 2, 3 };  
```  
When False  
```csharp  
var list = new List<int>();  
list.Add(1);  
list.Add(2);  
list.Add(3);  
```  

---
## 22. dotnet_style_explicit_tuple_names  
**Description**: Ensures tuple elements have explicit names.  
\
**Examples**  
When True  
```csharp  
(int Id, string Name) person = (1, "John");  
```  
When False  
```csharp  
(int, string) person = (1, "John");  
```  

---
## 23. dotnet_style_namespace_match_folder  
**Description**: Enforces that namespaces match the folder structure.  
\
**Examples**  
When True  
```csharp  
// File: MyProject/Utilities/Logger.cs  
namespace MyProject.Utilities;  
```  
When False  
```csharp  
// File: MyProject/Utilities/Logger.cs  
namespace SomeRandomName;  
```  

---
## 24. dotnet_style_null_propagation  
**Description**: Prefers `?.` operator over explicit null checks.  
\
**Examples**  
When True  
```csharp  
var length = str?.Length;  
```  
When False  
```csharp  
var length = str == null ? 0 : str.Length;  
```  

---
## 25. dotnet_style_object_initializer  
**Description**: Enforces using object initializers.  
\
**Examples**  
When True  
```csharp  
var person = new Person { Name = "Alice", Age = 30 };  
```  
When False  
```csharp  
var person = new Person();  
person.Name = "Alice";  
person.Age = 30;  
```  

---
## 26. dotnet_style_operator_placement_when_wrapping  
**Description**: Sets operator placement when wrapping lines.  
\
**Examples**  
Option 1 (beginning_of_line):  
```csharp  
var sum = a  
    + b  
    + c;  
```  
Option 2 (end_of_line):  
```csharp  
var sum = a +  
    b +  
    c;  
```  

---
## 27. dotnet_style_prefer_auto_properties  
**Description**: Prefers auto-properties over explicit backing fields.  
\
**Examples**  
When True  
```csharp  
public int Age { get; set; }  
```  
When False  
```csharp  
private int _age;  
public int Age { get => _age; set => _age = value; }  
```  

---
## 28. dotnet_style_prefer_collection_expression  
**Description**: Prefers collection expressions (e.g., `[1, 2, 3]`).  
\
**Examples**  
Option 1  
```csharp  
var list = [1, 2, 3];  
```  
Option 2  
```csharp  
var list = new List<int> { 1, 2, 3 };  
```  

---
## 29. dotnet_style_prefer_compound_assignment  
**Description**: Prefers compound assignment operators (e.g., `+=`).  
\
**Examples**  
When True  
```csharp  
x += 1;  
```  
When False  
```csharp  
x = x + 1;  
```  

---
## 30. dotnet_style_prefer_conditional_expression_over_assignment  
**Description**: Prefers conditional expressions over `if` statements for assignments.  
\
**Examples**  
When True  
```csharp  
var result = condition ? "Yes" : "No";  
```  
When False  
```csharp  
string result;  
if (condition) result = "Yes";  
else result = "No";  
```  

---
## 31. dotnet_style_prefer_conditional_expression_over_return  
**Description**: Prefers conditional expressions over `if` statements for returns.  
\
**Examples**  
When True  
```csharp  
return condition ? "Yes" : "No";  
```  
When False  
```csharp  
if (condition) return "Yes";  
return "No";  
```  

---
## 32. dotnet_style_prefer_foreach_explicit_cast_in_source  
**Description**: Prefers explicit casting in `foreach` loops when types are known.  
\
**Examples**  
Option 1  
```csharp  
foreach (string x in collectionOfObjects) { }  
```  
Option 2  
```csharp  
foreach (var x in collectionOfObjects.Cast<string>()) { }  
```  

---
## 33. dotnet_style_prefer_inferred_anonymous_type_member_names  
**Description**: Omits redundant property names in anonymous types.  
\
**Examples**  
When True  
```csharp  
var anon = new { FirstName, LastName };  
```  
When False  
```csharp  
var anon = new { FirstName = FirstName, LastName = LastName };  
```  

---
## 34. dotnet_style_prefer_inferred_tuple_names  
**Description**: Omits redundant tuple element names.  
\
**Examples**  
When True  
```csharp  
var person = (firstName, lastName);  
```  
When False  
```csharp  
var person = (firstName: firstName, lastName: lastName);  
```  

---
## 35. dotnet_style_prefer_is_null_check_over_reference_equality_method  
**Description**: Prefers `is null` over `ReferenceEquals(obj, null)`.  
\
**Examples**  
When True  
```csharp  
if (obj is null) { }  
```  
When False  
```csharp  
if (ReferenceEquals(obj, null)) { }  
```  

---
## 36. dotnet_style_prefer_simplified_boolean_expressions  
**Description**: Prefers simplified boolean expressions.  
\
**Examples**  
When True  
```csharp  
if (flag) { }  
```  
When False  
```csharp  
if (flag == true) { }  
```  

---
## 37. dotnet_style_prefer_simplified_interpolation  
**Description**: Prefers simplified string interpolation.  
\
**Examples**  
When True  
```csharp  
$"Hello {name}";  
```  
When False  
```csharp  
$"Hello {name.ToString()}";  
```  

---
## 38. dotnet_style_readonly_field  
**Description**: Enforces `readonly` for immutable fields.  
\
**Examples**  
When True  
```csharp  
private readonly int _count = 0;  
```  
When False  
```csharp  
private int _count = 0;  
```  

---
## 39. dotnet_code_quality_unused_parameters  
**Description**: Configures how unused parameters are handled.  
\
**Examples**  
Option 1 (align with interface):  
```csharp  
void IInterface.Method(int unused) { }  
```  
Option 2 (warning):  
```csharp  
void Method(int unused) { } // Warning  
```  

---
## 40. dotnet_remove_unnecessary_suppression_exclusions  
**Description**: Controls which suppressions are considered unnecessary.  

---
## 41. dotnet_style_allow_multiple_blank_lines_experimental  
**Description**: Controls whether multiple consecutive blank lines are allowed.  

---
## 42. dotnet_style_allow_statement_immediately_after_block_experimental  
**Description**: Controls whether statements can follow closing braces on the same line.  
\
**Examples**  
When True  
```csharp  
if (condition)  
{  
    DoSomething();  
} DoSomethingElse();  
```  
When False  
```csharp  
if (condition)  
{  
    DoSomething();  
}  
DoSomethingElse();  
```  

---
## 43. csharp_style_var_elsewhere  
**Description**: Controls `var` usage for non-built-in types.  
\
**Examples**  
When True  
```csharp  
int x = 0;  
```  
When False  
```csharp  
var x = 0;  
```  

---
## 44. csharp_style_var_for_built_in_types  
**Description**: Enforces `var` for built-in types.  
\
**Examples**  
When True  
```csharp  
var x = 0;  
```  
When False  
```csharp  
int x = 0;  
```  

---
## 45. csharp_style_var_when_type_is_apparent  
**Description**: Enforces `var` when the type is obvious.  
\
**Examples**  
When True  
```csharp  
var stream = new MemoryStream();  
```  
When False  
```csharp  
MemoryStream stream = new MemoryStream();  
```  

---
## 46. csharp_style_expression_bodied_accessors  
**Description**: Enforces expression-bodied syntax for property accessors.  
\
**Examples**  
When True  
```csharp  
public int Age => _age;  
```  
When False  
```csharp  
public int Age { get { return _age; } }  
```  

---
## 47. csharp_style_expression_bodied_constructors  
**Description**: Enforces expression-bodied syntax for constructors.  
\
**Examples**  
When True  
```csharp  
public Person() => Name = "Unknown";  
```  
When False  
```csharp  
public Person()  
{  
    Name = "Unknown";  
}  
```  

---
## 48. csharp_style_expression_bodied_indexers  
**Description**: Enforces expression-bodied syntax for indexers.  
\
**Examples**  
When True  
```csharp  
public int this[int index] => _items[index];  
```  
When False  
```csharp  
public int this[int index]  
{  
    get { return _items[index]; }  
}  
```  

---
## 49. csharp_style_expression_bodied_lambdas  
**Description**: Enforces expression-bodied syntax for lambdas.  
\
**Examples**  
When True  
```csharp  
var func = x => x * 2;  
```  
When False  
```csharp  
var func = x =>  
{  
    return x * 2;  
};  
```  

---
## 50. csharp_style_expression_bodied_local_functions  
**Description**: Enforces expression-bodied syntax for local functions.  
\
**Examples**  
When True  
```csharp  
int Sum(int a, int b) => a + b;  
```  
When False  
```csharp  
int Sum(int a, int b)  
{  
    return a + b;  
}  
```  

---
## 51. csharp_style_expression_bodied_methods  
**Description**: Enforces expression-bodied syntax for methods.  
\
**Examples**  
When True  
```csharp  
public int GetValue() => 42;  
```  
When False  
```csharp  
public int GetValue()  
{  
    return 42;  
}  
```  

---
## 52. csharp_style_expression_bodied_operators  
**Description**: Enforces expression-bodied syntax for operator overloads.  
\
**Examples**  
When True  
```csharp  
public static Vector operator +(Vector a, Vector b) => new(a.X + b.X, a.Y + b.Y);  
```  
When False  
```csharp  
public static Vector operator +(Vector a, Vector b)  
{  
    return new Vector(a.X + b.X, a.Y + b.Y);  
}  
```  

---
## 53. csharp_style_expression_bodied_properties  
**Description**: Enforces expression-bodied syntax for properties.  
\
**Examples**  
When True  
```csharp  
public int MyProperty => _myField;  
```  
When False  
```csharp  
public int MyProperty  
{  
    get { return _myField; }  
}  
```  

---
## 54. csharp_style_pattern_matching_over_as_with_null_check  
**Description**: Prefers pattern matching over `as` + null check.  
\
**Examples**  
When True  
```csharp  
if (obj is MyClass c) { }  
```  
When False  
```csharp  
var c = obj as MyClass;  
if (c != null) { }  
```  

---
## 55. csharp_style_pattern_matching_over_is_with_cast_check