# DSPD_TREES
A step tracking application lets a user calculate daily steps, set goals for a week, create groups to
achieve group goals, and gives rewards to individuals who complete their goals. It also maintains
leader boards to encourage people to complete steps with great rewards for top 3 individuals. It also
has a group leader board where groups are ranked according to steps completed by each group as a
whole. We have to design this step tracking application using trees.

1. Generate a tree of individuals with following fields
a. ID (unique ID)
b. Name
c. Age
d. Daily Step goal
e. Array of weekly step count (7 days step count recorded)
This tree should be sorted on the basis of ID.

2. Generate a tree of groups with following fields
a. Group-ID
b. Group name
c. Member IDs with pointers to individuals in individuals tree
d. Weekly group goal
This tree should be sorted on the basis of Group-ID. A group can contain maximum 5
individuals.

The application should have the following functionalities
a. Add_Person: This function should add a new individual to the tree of individuals. The
tree should remain sorted

b. Create_group: This function should create a new group and be able to add existing
individuals to it from the individual tree. If an individual already belongs to a group,
he cannot be added to a new group.

c. Get_top_3: this function should display the top 3 individuals from the individual tree
who have completed their daily steps goals and achieved highest number of steps.
The individuals who have not completed daily goals but have higher number of steps
should be excluded.

d. Check_group_achievement(Group-ID): This function should display whether the
given group has completed its weekly group goal

e. Generate_leader_board: This function should take the group tree, sort it in the
order of highest number of steps (Descending) completed by each group such that
the root of the tree has the leading group, and display the group name with number
of steps based on rank using this sorted tree.

f. Check_individual_rewards(ID): This function should display the rewards earned by
the given individual if he is in the top 3 individuals. Rank 1 gets 100 points, rank 2
gets 75 points, and rank 3 gets 50 points

g. Delete_individual(ID): This function should delete an individual from the tree of
individuals as well as remove him from his groups.

h. Delete_group(Group-ID): This function should delete a group but retain its
individuals. The individuals are now available to be added to a different group

i. Merge_groups(Group_ID_1, Group_ID_2): Create a new group by merging two
groups and set new goals. The original groups should be deleted. The group should
be merged with group_ID_1 as new ID and group_ID_2 should be deleted.

j. Display_group_range_info(): This function should take input as two group ids and
display information about members in the range of these groups as well as group
goals and ranks.

k. Suggest_goal_update(): This function should suggest a daily goal update for an
individual such that he/she can consistently appear in the top 3 individuals

