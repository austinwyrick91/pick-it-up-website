import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";
import { CalendarIcon, HeartHandshake, MailIcon } from "lucide-react";

export default function HomePage() {
  return (
    <div className="bg-white text-gray-900">
      {/* Hero Section */}
      <section className="bg-gray-100 py-20 px-4 text-center">
        <motion.h1
          className="text-4xl md:text-6xl font-bold mb-4"
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
        >
          Cleaning Las Vegas from the Underground Up
        </motion.h1>
        <p className="text-lg md:text-xl mb-6 max-w-2xl mx-auto">
          Join our grassroots movement to clean up the tunnels and streets of our city and support those affected by homelessness and addiction.
        </p>
        <div className="flex justify-center gap-4 flex-wrap">
          <Button size="lg">Get Involved</Button>
          <Button size="lg" variant="outline">Donate</Button>
        </div>
      </section>

      {/* About Strip */}
      <section className="py-16 px-6 bg-white text-center">
        <h2 className="text-3xl font-semibold mb-4">Who We Are</h2>
        <p className="max-w-3xl mx-auto text-lg">
          The Pick It Up Foundation is a nonprofit based in Las Vegas dedicated to cleaning up urban waste, engaging volunteers, and providing outreach to the homeless community—especially those in the tunnels.
        </p>
        <div className="mt-6">
          <Button>Our Mission</Button>
        </div>
      </section>

      {/* Events & Impact */}
      <section className="bg-gray-50 py-16 px-4 text-center">
        <h2 className="text-3xl font-semibold mb-8">Upcoming Events</h2>
        <div className="flex justify-center">
          <Card className="max-w-md w-full text-left">
            <CardContent className="p-6">
              <div className="flex items-center gap-2 text-sm text-gray-500 mb-2">
                <CalendarIcon className="w-4 h-4" />
                Saturday, April 13 @ 9 AM
              </div>
              <h3 className="text-xl font-bold mb-2">Tunnel Cleanup: Spring Valley</h3>
              <p className="mb-4 text-gray-700">
                Join our volunteers for a cleanup in one of Las Vegas’ largest tunnel systems. All gear provided. Sign up now!
              </p>
              <Button>Join Us</Button>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* CTA Banner */}
      <section className="bg-black text-white py-12 px-4 text-center">
        <h2 className="text-3xl font-semibold mb-6">Be the Change You Want to See in Vegas</h2>
        <div className="flex justify-center gap-4 flex-wrap">
          <Button size="lg" className="bg-green-600 hover:bg-green-700">
            <HeartHandshake className="mr-2 w-5 h-5" /> Get Involved
          </Button>
          <Button size="lg" variant="outline" className="text-white border-white hover:bg-white hover:text-black">
            Donate Now
          </Button>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-100 text-center py-8 px-4">
        <p className="mb-2">&copy; {new Date().getFullYear()} The Pick It Up Foundation</p>
        <div className="flex justify-center gap-4">
          <a href="#" className="text-gray-600 hover:text-black">Instagram</a>
          <a href="#" className="text-gray-600 hover:text-black">Facebook</a>
          <a href="#contact" className="text-gray-600 hover:text-black">Contact</a>
        </div>
      </footer>
    </div>
  );
}
