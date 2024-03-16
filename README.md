#include<iostream>
class Person{
private:
float age;
std::string name;
std::string gender;
public:
Person(std::string name, std::string gender, float age) : name(name), gender(gender), age(age) {}
Person() : name("  "), gender("  "), age(00) {}
void set_age (float a){
age=a;
}
void set_name (std::string n){
    name =n;
}
void set_gender (std::string g){
    gender = g;
    }

float get_age (){
return age;
}
std::string get_name (){
    return name;
}
std::string get_gender (){
    return gender;
    }

};
class Student : public Person{

private:
float id;
std::string major;
float gpa;
public:
Student(std::string major, float  id, float gpa) : major(major), id(id), gpa(gpa) {}

Student() : major("n/a"), id(00000), gpa(0.0)
{
}
void set_id (float i){
id=i;
}
void set_major (std::string m){
    major =m;

}
void set_gpa (float  g){
    gpa = g;
    }

float get_id (){
return id;
}
std::string get_major (){
    return major;
}
float get_gpa (){
    return gpa;
    }



};
class Em : public Person{

private:
float salary;
std::string jop;
float rank;
public:
Em(std::string jop, float  rank, float salary) : jop(jop), salary(salary), rank(rank) {}

Em() : jop("n/a"), rank(00000), salary(0.0)
{
}
void set_rank (float r){
rank=r;
}
void set_jop (std::string j){
    jop =j;

}
void set_salary (float  s){
    salary = s;
    }



float get_salary (){
return salary;
}
std::string get_jop (){
    return jop;
}
float get_rank (){
    return rank;
    }
};
int main (){
Person p;
Student s;
Em e;

p.set_age(14);
p.set_name ("anas");
p.set_gender ("male");

s.set_major("eng");
s.set_id (23232);
s.set_gpa (4.00);

e.set_jop("it");
e.set_salary(300000);
e.set_rank(3);
std::cout<<" age is "<<p.get_age()<<std::endl;
std::cout<<" name is "<<p.get_name()<<std::endl;
std::cout<<" gender is "<<p.get_gender()<<std::endl;

std::cout<<" major is "<<s.get_major()<<std::endl;
std::cout<<" id is "<<s.get_id()<<std::endl;
std::cout<<" gpa is "<<s.get_gpa()<<std::endl;

std::cout<<" jop is "<<e.get_jop()<<std::endl;
std::cout<<" name is "<<e.get_rank()<<std::endl;
std::cout<<" salary is "<<e.get_salary()<<std::endl;



}
