class Node

    attr_accessor :value, :next_node

    def initialize val,next_in_line
        @value = val
        @next_nodex = next_in_line
    end
end

class LinkedList

    def initialize val
        # New node 
        @head = Node.new(val,nil)
    end
    
    def add(value)
        # Traverse the linked list and insert a new node at the tail
        current = @head
        while current.next_node != nil # Keep going forward while it dont reaches the end of the list
            current = current.next_node #Advance to the next node in the list
        end 
        current.next_node = Node.new(value,nil) #Attach the new node
        self    
    end

    def delete(val)
        current = @head
        if current.value == val #If we need to delete the head element. We only update the head 
        # For example if we consider:
        #x->y and we wanted to delete x, now we let y to be the new head
            @head = @head.next_node
        else
            #If we consider the following:
            # ... x -> y -> z
            # We need to reshape the list to be like this:
            #   ... x->z
            # where z is y.next_node
            current = @head
            while (current != nil) && (current.next_node != nil) && ((current.next_node).value != val)
                current = current.next_node
            end 

            if (current != nil) && (current.next_node != nil)
                current.next_node = (current.next_node).next_node
            end
        end
    end
    
    def display
        # Traverse through the list till you hit the "nil" at the end (null value)
        current = @head
        full_list = [] 
        while current.next_node != nil 
            full_list += [current.value.to_s]
            current = current.next_node
        end
        full_list += [current.value.to_s]
        puts full_list.join("\n")
        
    end

end

temp = gets.chomp.to_i
ll = LinkedList.new(temp)
# Adding Elements to Linked List
temp.to_i
u = 0 + temp
z = 0 - 1 #We do this to let ruby know that our variable must be taken as an int, and not as a char.
while temp.to_i != z #While the user dont try to add a -1 to the list

    temp = gets.chomp
    if temp.to_i != -1 #This is a filter, because we dont want to add the -1 to the list
        ll.add(temp)
    end

    temp.to_i
end
    

# Print the created linked list
puts "Your linked list is:"
ll.display

#If we need to delete an element, we occupy ll.delete('element to delete')
