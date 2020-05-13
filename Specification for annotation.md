# Specification for annotation

## 1 - Definition of "Building Parts"

The "named entity" marked "building parts" can be subdivided into:
  
     (1) Phrases that indicates location, such as: Area A, the 5th floor, bottom of the hole;
  
     (2) Words or phrases representing building components, such as: stairs, the 10# tower crane, upper stirrups, reinforcement mesh, artificially digging piles, high formwork, reinforcement connection, reinforcement thread;
  
     (3) Words representing building materials, such as: concrete and steel;
  
     (4) Phrases formed by adding “location suffix” to building components, such as: **around** #10 crane, **bottom** of cantilever beam, high formwork **area**, stair**well**;
  
## 2 - Labeling Rules

    （1）Tags "B", "I", and "O" are used to mark the "named entities" in the corpus. **‘B’** stands for the beginning of the named entity, **‘I’** stands for the other parts of the named entity, and **‘O’** stands for the words that do not belong to the “named entity”. The following are examples of annotations:
    
    （2）When labeling corpus, the following situation often occurs: "named entities" are arranged consecutively, such as: "the stirrup at the bottom of the 5-layer cantilever beam in Area A" (A区5层悬挑梁底部箍筋), at this time, the string needs to be effectively split into multiple Named entities". The principles of separation are:
    
        ①Take the "location" suffix in the table as the split indicator. For example, in the string "hoop stirrups at the bottom of the 5-layer cantilever beam in Area A" (A**区**5**层**悬挑梁**底部**箍筋), the suffixes in the table position are "Area" (区), "Layer"（层） and "Bottom"（底部）, then the phrase should be split into "Area A" (A区), "5-layer"（5层）, "Bottom of cantilever beam"（悬挑梁底部）and "hoop stirrup" （箍筋）.
        
        ②For the case in which there is no suffix in the table position. For example, though "cantilever beam stirrup" (悬挑梁箍筋) can be divided into "cantilever beam" and "stirrup", it should be still treated as a hole named entity.

## 3 - Tricks for annotation

Since the number of tags “O” that need to be marked contributes is large, you can mark “B” and “I” only without “O”.

## 4 - Remarks

If there are any cases you are not sure how to label during the labeling process, please communicate with your team.
