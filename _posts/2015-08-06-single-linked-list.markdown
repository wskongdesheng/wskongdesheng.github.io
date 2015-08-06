---
layout: post
title: 'single linked list ruby'
date: 2015-08-06 15:01:00
categories: ruby
---
{% highlight ruby %}
class Node
  attr_accessor :value, :next

  def initialize(value = nil)
    @value = value
  end

  def to_s
    @value
  end
end

class SinglyLinkedList

  attr_accessor :head

  def initialize(first_value=nil)
    @head = Node.new(first_value) if first_value
  end

  def add(value)
    if head.nil?
      head = Node.new(value)
    else
      current_node = @head
      while current_node.next
        current_node = current_node.next
      end
      current_node.next = Node.new(value)
    end
  end
  def find(value)
    current_node = head
    while current_node != nil
      return current_node if current_node.value == value
      current_node = current_node.next
    end
    nil
  end

  def remove(value)
    if head.value == value
      head = head.next
    else
      current_node = head.next
      prev_node = head
      while current_node
        if current_node.value == value
          prev_node.next = current_node.next
          return true
        end
        prev_node = current_node
        current_node = current_node.next
      end
      nil
    end
  end
end
{% endhighlight %}
