Diagram Design
==============

* Tips on designing diagrams to elucidate understanding
* Diagrams to describe structure
* Diagrams to describe work flow
* Use of ERD and/or UML - more formalised
* Blockdiag/Graphviz whilst more intuitive for the non-technical can be more verbose to be more accurate

Design Tips
--------------

How to use different diagram types to demonstrate and clarify the subject matter.  Which type of diagram works best to describe structure, workflow etc.


Diagram Types
-------------

ERD - Entity Relationship Diagram
*********************************

* `Guru99 ERD tutorial <https://www.guru99.com/er-diagram-tutorial-dbms.html>`_

UML - Unified Modeling Language
*********************************

* References
   * `Tutorials Point UML Tutorial <https://www.tutorialspoint.com/uml/uml_overview.htm>`_
   * `PlantUML Tutorial <https://crashedmind.github.io/PlantUMLHitchhikersGuide/layout/layout.html>`_ also good example of RTD on github.io  
* Fundamental object-oriented concepts
   * Objects − represent an entity
   * Class − blue print of an object.
   * Abstraction − behavior of an real world entity.
   * Encapsulation − binding the data together and hiding them from the outside world.
   * Inheritance − making new classes from existing ones.
   * Polymorphism − existence in different forms.
* Building Blocks
   * Things
      * Structural - static - class, interface, collaboration, use case, component, node
      * Behavioural - dynamic - interaction, state machine
      * Grouping - grouping - package
      * Annotational - remarks, description, comments - note
   * Relationships - associations between elements
      * Dependency - change in one element affects the other
      * Association - element connections and counts
      * Generalisation - connection from generalised to specialised element  
      * Realisation - connection from responsibility element to implementation element  
   * Diagrams - the output of the process
      * Class - abstract components
      * Object - real components, point in time
      * Component - underlying structure of a component - physical s/w - source code, runtime and executables
      * Composite Structure - internal structure of class
      * Deployment - physical resources nodes, components and connections
      * Package - organise elements into related groups to minimise dependecies between packages
      * Profile - extensibility mechanism
      * Activity - flow and relationship of activities/actions, objects used/consumed/produced
      * Use case - functional requirements, actors, relationships 
      * Interaction Overview - combination of activity and sequence diagrams
      * Timing - object relationships over time, time left to right
      * State Machine (statechart) - different states of component within the system
      * Communication (Collaboration) - interaction between objects in sequence
      * Sequence - sequence of messages/interactions between actors and objects over time
* Architecture
   * System perspectives - diagram use case
      * Design - classes, interfaces, collaboration - diagrams class, object
      * Implementation - component assembly for complete physical system - diagram component
      * Process - system flow - diagrams class, object
      * Deployment - physical nodes forming hardware - diagram deployment  
* Modeling Types
   * Structural Modeling - static features, framework - diagrams class, component, deployment
   * Behavioural Modeling - interaction, sequence, flow - diagrams activity, interaction, use case  
   * Architectural Modeling - overall framework including structure and behaviour - diagram package  
* Basic Notations
   * Structural
      * Class
      * Object
      * Interface
      * Collaboration
      * Use Case
      * Actor
      * Initial State
      * Final State
      * Active Class
      * Component
      * Node
   * Behavioural
      * Interaction
      * State Machine
   * Grouping
      * Package
   * Annotational
      * Note
   * Relationships
      * Instance Level
         * Dependency - 2+ elements depend on each other, dashed line/open arrow, unidirectional
         * Association - connect 2+ elements in model, solid line/open arrow
            * Types - bi-directional, uni-directional, aggregation, reflexive
         * Aggregation - "has a", binary, solid line/open diamond
         * Composition - whole/part relationship, when higher is destroyed so is lower, solid line/closed diamond
      * Class Level
         * Generalisation/Inheritance - superclass (generalised), subclass (specialised) - hollow triangle on supertype, subclass inherits attributes/methods of superclass
         * Realisation/Implementation/Abstraction - client realises/implements behaviour the supplier specifies - hollow triangle on interface/dashed line (DRY)
      * General Relationship
         * Dependency - one class depends on another at some point in time e.g. independent class is parameter variable of a method of dependent class
      * Multiplicity - 0, 0..1, 1..1, * (zero or more), 1..* (one or more) etc.

.. include:: diagram.design/relationships.snippet.rst
* Standard Diagrams
* Class Diagram
   * name - meaningful aspect of the system
   * attributes - values describing an instance of the class
   * methods - responsibilities, behavioural features
   * relationships
   * visibility - private(-), public(+), protected(#) subclass, package/default(~)     
* Object Diagram
   * derived from class diagrams - instance of a class, snapshot of point in time
   * class abstract, object concrete  
   * name - indicates purpose
   * attribute - state of a particular instance  
* Component Diagram
* Deployment Diagram
* Use Case Diagram
* Interaction Diagram
* State Chart Diagram
* Activity Diagram
* Summary

RST/Sphinx Implementation
-------------------------

UML Relationships Diagram

.. literalinclude:: diagram.design/relationships.snippet.rst
   :language: rst
