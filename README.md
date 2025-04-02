import React from "react";
import { motion } from "framer-motion";

export default function Home() {
  return (
    <div className="flex flex-col items-center justify-center min-h-screen bg-black text-white">
      {/* Navigation Bar */}
      <nav className="w-full flex justify-between items-center p-6 bg-gray-900">
        <motion.h2
          className="text-2xl font-semibold"
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ duration: 1 }}
        >
          KINGVON
        </motion.h2>
        <ul className="flex space-x-6">
          <li className="hover:text-blue-400 transition cursor-pointer">Home</li>
          <li className="hover:text-blue-400 transition cursor-pointer">About</li>
          <li className="hover:text-blue-400 transition cursor-pointer">Services</li>
          <li className="hover:text-blue-400 transition cursor-pointer">Contact</li>
        </ul>
      </nav>

      {/* Hero Section */}
      <motion.h1
        className="text-5xl font-bold mt-12"
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        KINGVON
      </motion.h1>
      <p className="mt-4 text-lg">Welcome to the Business Hub</p>
      <button className="mt-6 px-6 py-3 bg-blue-500 rounded-lg hover:bg-blue-600 transition">
        Get Started
      </button>

      {/* Additional Section */}
      <section className="mt-12 w-full px-10 text-center">
        <h2 className="text-3xl font-semibold">Our Services</h2>
        <div className="grid grid-cols-1 md-grid-cols-3 gap-6 mt-6">
          <div className="p-6 bg-gray-800 rounded-lg hover:scale-105 transition">
            <h3 className="text-xl font-bold">Web Development</h3>
            <p className="text-gray-400">Building modern and responsive websites.</p>
          </div>
          <div className="p-6 bg-gray-800 rounded-lg hover:scale-105 transition">
            <h3 className="text-xl font-bold">SEO Optimization</h3>
            <p className="text-gray-400">Enhancing your online visibility.</p>
          </div>
          <div className="p-6 bg-gray-800 rounded-lg hover:scale-105 transition">
            <h3 className="text-xl font-bold">Branding</h3>
            <p className="text-gray-400">Creating a unique identity for your business.</p>
          </div>
        </div>
      </section>

      {/* Contact Form */}
      <section className="mt-12 w-full px-10 text-center">
        <h2 className="text-3xl font-semibold">Contact Us</h2>
        <form className="mt-6 max-w-lg mx-auto bg-gray-900 p-6 rounded-lg">
          <div className="mb-4">
            <label className="block text-left mb-2">Name</label>
            <input 
              type="text" 
              className="w-full p-2 rounded bg-gray-800 border border-gray-600 focus:outline-none focus:border-blue-400"
              placeholder="KINGVON"
              value="KINGVON"
              readOnly
            />
          </div>
          <div className="mb-4">
            <label className="block text-left mb-2">Email</label>
            <input 
              type="email" 
              className="w-full p-2 rounded bg-gray-800 border border-gray-600 focus:outline-none focus:border-blue-400"
              placeholder="silvertosh24@gmail.com"
              value="silvertosh24@gmail.com"
              readOnly
            />
          </div>
          <div className="mb-4">
            <label className="block text-left mb-2">Phone</label>
            <input 
              type="text" 
              className="w-full p-2 rounded bg-gray-800 border border-gray-600 focus:outline-none focus:border-blue-400"
              placeholder="0720326316"
              value="0720326316"
              readOnly
            />
          </div>
          <div className="mb-4">
            <label className="block text-left mb-2">Message</label>
            <textarea 
              className="w-full p-2 rounded bg-gray-800 border border-gray-600 focus:outline-none focus:border-blue-400"
              rows="4"
              placeholder="Enter your message"
            ></textarea>
          </div>
          <button 
            type="submit" 
            className="w-full p-3 bg-blue-500 rounded-lg hover:bg-blue-600 transition"
          >
            Send Message
          </button>
        </form>
      </section>
    </div>
  );
}
