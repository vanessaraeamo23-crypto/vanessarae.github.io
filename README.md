import React from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 p-6">
      {/* Hero Section */}
      <section className="text-center py-16">
        <motion.h1
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          className="text-4xl font-bold"
        >
          Hi, I'm Your Name
        </motion.h1>
        <p className="mt-4 text-lg">Creative Professional | Designer | Developer</p>
        <Button className="mt-6">Download Resume</Button>
      </section>

      {/* About Section */}
      <section className="max-w-3xl mx-auto py-12">
        <h2 className="text-2xl font-semibold mb-4">About Me</h2>
        <p>
          I am a passionate individual with experience in design, development, and customer service. I love building beautiful and functional digital experiences.
        </p>
      </section>

      {/* Projects Section */}
      <section className="py-12">
        <h2 className="text-2xl font-semibold text-center mb-8">Projects</h2>
        <div className="grid md:grid-cols-3 gap-6">
          {[1, 2, 3].map((project) => (
            <Card key={project} className="rounded-2xl shadow-md">
              <CardContent className="p-4">
                <h3 className="font-semibold text-lg">Project {project}</h3>
                <p className="text-sm mt-2">Short description of your project.</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Contact Section */}
      <section className="text-center py-12">
        <h2 className="text-2xl font-semibold mb-4">Contact Me</h2>
        <p>Email: your@email.com</p>
      </section>
    </div>
  );
}
