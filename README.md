import React, { useState } from 'react';

// Main App Component
const App = () => {
    const [currentPage, setCurrentPage] = useState('home'); // State to manage current page

    // Function to navigate between pages
    const navigateTo = (page) => {
        setCurrentPage(page);
    };

    // Header Component for navigation
    const Header = ({ navigateTo }) => {
        return (
            <header className="bg-stone-100 shadow-md py-4 px-6 fixed w-full z-10 top-0 rounded-b-lg">
                <nav className="container mx-auto flex flex-col md:flex-row justify-between items-center">
                    {/* Logo and Site Title */}
                    <div className="flex items-center mb-4 md:mb-0">
                        <img src="https://placehold.co/40x40/BFE0F7/0A2C59?text=DE" alt="DigiEnd Logo" className="rounded-full mr-3"/>
                        <h1 className="text-3xl font-extrabold text-blue-800 tracking-tight">DigiEnd</h1>
                    </div>
                    {/* Navigation Links */}
                    <ul className="flex flex-wrap justify-center space-x-4 md:space-x-8 text-lg font-medium">
                        <li>
                            <button
                                onClick={() => navigateTo('home')}
                                className="text-stone-700 hover:text-blue-600 transition-colors duration-300 px-3 py-2 rounded-md"
                            >
                                Home
                            </button>
                        </li>
                        <li>
                            <button
                                onClick={() => navigateTo('about')}
                                className="text-stone-700 hover:text-blue-600 transition-colors duration-300 px-3 py-2 rounded-md"
                            >
                                About Us
                            </button>
                        </li>
                        <li>
                            <button
                                onClick={() => navigateTo('services')}
                                className="text-stone-700 hover:text-blue-600 transition-colors duration-300 px-3 py-2 rounded-md"
                            >
                                Our Services
                            </button>
                        </li>
                        <li>
                            <button
                                onClick={() => navigateTo('contact')}
                                className="text-stone-700 hover:text-blue-600 transition-colors duration-300 px-3 py-2 rounded-md"
                            >
                                Contact Us
                            </button>
                        </li>
                    </ul>
                </nav>
            </header>
        );
    };

    // Footer Component
    const Footer = () => {
        return (
            <footer className="bg-blue-50 py-8 mt-12 text-center text-blue-800 rounded-t-lg shadow-inner">
                <div className="container mx-auto px-4">
                    <p className="text-lg mb-2">&copy; {new Date().getFullYear()} DigiEnd. All rights reserved.</p>
                    <p className="text-sm">Driven by Market Research, Not Book Knowledge.</p>
                </div>
            </footer>
        );
    };

    // Home Page Component
    const HomePage = () => {
        return (
            <div className="pt-24 pb-8 bg-gradient-to-br from-beige-light to-blue-light text-stone-800">
                <div className="container mx-auto px-6">
                    {/* Hero Section */}
                    <section className="text-center py-16 bg-blue-50 rounded-2xl shadow-xl mb-12">
                        <h2 className="text-5xl md:text-6xl font-extrabold text-blue-800 mb-6 leading-tight">
                            DigiEnd: Your End-to-End Digital Marketing Solution
                        </h2>
                        <p className="text-xl md:text-2xl text-stone-700 max-w-3xl mx-auto mb-8">
                            Empowering your business with data-driven strategies for sales, lead generation, branding, and awareness.
                        </p>
                        <button className="bg-blue-600 text-white font-bold py-4 px-10 rounded-full text-xl shadow-lg hover:bg-blue-700 transform hover:scale-105 transition duration-300">
                            Get a Free Consultation
                        </button>
                    </section>

                    {/* USP Section */}
                    <section className="py-16 text-center">
                        <h3 className="text-4xl font-bold text-blue-700 mb-8">Our Unique Selling Proposition</h3>
                        <div className="flex flex-col md:flex-row items-center bg-stone-100 rounded-2xl shadow-lg p-8">
                            <div className="md:w-1/2 md:pr-8 mb-6 md:mb-0">
                                <img src="https://placehold.co/600x400/D4C9B9/4A4A4A?text=Market+Research" alt="Market Research" className="rounded-xl shadow-md"/>
                            </div>
                            <div className="md:w-1/2 text-left">
                                <p className="text-2xl text-stone-700 leading-relaxed">
                                    At DigiEnd, we don't rely on generic strategies or "book knowledge." Our solutions are crafted
                                    from in-depth <strong className="text-blue-800">market research and real-world insights</strong>.
                                    We analyze your specific industry, target audience, and competitive landscape to deliver
                                    strategies that truly convert and drive growth.
                                </p>
                            </div>
                        </div>
                    </section>

                    {/* Services Overview Section */}
                    <section className="py-16 text-center">
                        <h3 className="text-4xl font-bold text-blue-700 mb-12">Our Core Expertise</h3>
                        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                            {/* Service Card 1: Google Ads */}
                            <div className="bg-stone-100 p-8 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/ADD8E6/000?text=GA" alt="Google Ads Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-4">Google Ads Mastery</h4>
                                <p className="text-lg text-stone-700">
                                    Maximize your reach and conversions with expertly managed Google Search, Display, and Shopping campaigns.
                                </p>
                            </div>
                            {/* Service Card 2: Meta Ads */}
                            <div className="bg-stone-100 p-8 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/87CEEB/000?text=MA" alt="Meta Ads Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-4">Meta Ads Excellence</h4>
                                <p className="text-lg text-stone-700">
                                    Drive engagement and sales across Facebook and Instagram with compelling ad creatives and precise targeting.
                                </p>
                            </div>
                            {/* Service Card 3: End-to-End Solutions */}
                            <div className="bg-stone-100 p-8 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/6A5ACD/000?text=ES" alt="End Solution Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-4">Complete Sales & Lead Gen</h4>
                                <p className="text-lg text-stone-700">
                                    From strategy to execution, we provide holistic solutions for sales optimization and consistent lead generation.
                                </p>
                            </div>
                        </div>
                    </section>

                    {/* Video Section - Placeholder for a promotional video */}
                    <section className="py-16 text-center bg-blue-50 rounded-2xl shadow-xl mb-12">
                        <h3 className="text-4xl font-bold text-blue-700 mb-8">See How We Deliver Results</h3>
                        <div className="relative w-full max-w-4xl mx-auto overflow-hidden rounded-xl shadow-lg" style={{ paddingTop: '56.25%' }}>
                            {/* Example placeholder for an embedded video (e.g., YouTube) */}
                            {/* Replace with your actual video embed code */}
                            <iframe
                                className="absolute top-0 left-0 w-full h-full"
                                src="https://www.youtube.com/embed/dQw4w9WgXcQ" // Placeholder for a YouTube video
                                title="YouTube video player"
                                frameBorder="0"
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                                allowFullScreen
                            ></iframe>
                        </div>
                        <p className="text-lg text-stone-700 mt-8">
                            Watch our video to understand our unique approach and how we can elevate your digital presence.
                        </p>
                    </section>
                </div>
            </div>
        );
    };

    // About Us Page Component
    const AboutUsPage = () => {
        return (
            <div className="pt-24 pb-8 bg-gradient-to-br from-beige-light to-blue-light text-stone-800">
                <div className="container mx-auto px-6">
                    <h2 className="text-5xl font-extrabold text-blue-800 text-center mb-12">About DigiEnd</h2>

                    {/* Our Philosophy */}
                    <section className="bg-stone-100 rounded-2xl shadow-xl p-8 mb-12">
                        <h3 className="text-4xl font-bold text-blue-700 mb-6 text-center">Our Philosophy: Beyond the Textbook</h3>
                        <div className="flex flex-col md:flex-row items-center">
                            <div className="md:w-1/2 md:pr-8 mb-6 md:mb-0">
                                <img src="https://placehold.co/600x400/D4C9B9/4A4A4A?text=Real-World+Insights" alt="Team collaborating" className="rounded-xl shadow-md"/>
                            </div>
                            <div className="md:w-1/2 text-left">
                                <p className="text-lg text-stone-700 leading-relaxed mb-4">
                                    At DigiEnd, we firmly believe that true digital marketing success stems from a deep understanding
                                    of the market, not just theoretical knowledge. While books provide foundational principles,
                                    the ever-evolving digital landscape demands agility, continuous learning, and strategies
                                    forged in the crucible of real-world campaigns.
                                </p>
                                <p className="text-lg text-stone-700 leading-relaxed">
                                    Our philosophy is simple: <strong className="text-blue-800">research, analyze, adapt, and execute.</strong>
                                    We dive deep into your industry, your competitors, and your audience's behavior to uncover
                                    unique opportunities and tailor-made solutions that deliver tangible results.
                                </p>
                            </div>
                        </div>
                    </section>

                    {/* Our Team Section */}
                    <section className="bg-blue-50 rounded-2xl shadow-xl p-8 mb-12">
                        <h3 className="text-4xl font-bold text-blue-700 mb-8 text-center">Meet Our Expert Team</h3>
                        <p className="text-lg text-stone-700 text-center mb-10 max-w-3xl mx-auto">
                            Our team is composed of seasoned digital marketing specialists, each bringing unique expertise in their
                            respective fields. We work collaboratively to ensure every aspect of your campaign is optimized for success.
                        </p>
                        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                            {/* Team Member 1: Varun Shrivastava */}
                            <div className="bg-stone-100 p-6 rounded-xl shadow-lg text-center transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/150x150/D4C9B9/4A4A4A?text=Varun+S" alt="Varun Shrivastava" className="rounded-full w-32 h-32 mx-auto mb-4 object-cover"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-2">Varun Shrivastava</h4>
                                <p className="text-blue-600 text-lg mb-3">Head of Strategy & Marketing Expert</p>
                                <p className="text-stone-700 text-base">
                                    With over 6 years of experience, Varun leads our strategic initiatives and is a seasoned marketing expert.
                                </p>
                            </div>
                            {/* Team Member 2: John Smith (retained as generic Google Ads Expert) */}
                            <div className="bg-stone-100 p-6 rounded-xl shadow-lg text-center transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/150x150/D4C9B9/4A4A4A?text=John+S" alt="John Smith" className="rounded-full w-32 h-32 mx-auto mb-4 object-cover"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-2">John Smith</h4>
                                <p className="text-blue-600 text-lg mb-3">Google Ads Expert</p>
                                <p className="text-stone-700 text-base">
                                    John's expertise lies in optimizing Google Ads campaigns for maximum performance and cost-efficiency.
                                </p>
                            </div>
                            {/* Team Member 3: Govind Mishra */}
                            <div className="bg-stone-100 p-6 rounded-xl shadow-lg text-center transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/150x150/D4C9B9/4A4A4A?text=Govind+M" alt="Govind Mishra" className="rounded-full w-32 h-32 mx-auto mb-4 object-cover"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-2">Govind Mishra</h4>
                                <p className="text-blue-600 text-lg mb-3">Social Media Specialist & Web Developer</p>
                                <p className="text-stone-700 text-base">
                                    Govind brings creative flair to social media and is an astonishing web developer with 4+ years of experience.
                                </p>
                            </div>
                        </div>
                    </section>

                    {/* Our Vision */}
                    <section className="bg-stone-100 rounded-2xl shadow-xl p-8">
                        <h3 className="text-4xl font-bold text-blue-700 mb-6 text-center">Our Vision</h3>
                        <p className="text-lg text-stone-700 leading-relaxed text-center max-w-4xl mx-auto">
                            Our vision at DigiEnd is to be the leading digital marketing partner for businesses seeking
                            unconventional, effective, and results-driven strategies. We aim to transform how businesses
                            connect with their audience, ensuring sustainable growth and a powerful online presence through
                            innovative, market-led solutions.
                        </p>
                    </section>
                </div>
            </div>
        );
    };

    // Services Page Component
    const ServicesPage = () => {
        return (
            <div className="pt-24 pb-8 bg-gradient-to-br from-beige-light to-blue-light text-stone-800">
                <div className="container mx-auto px-6">
                    <h2 className="text-5xl font-extrabold text-blue-800 text-center mb-12">Our Comprehensive Services</h2>

                    <section className="bg-stone-100 rounded-2xl shadow-xl p-8 mb-12">
                        <h3 className="text-4xl font-bold text-blue-700 mb-8 text-center">End-to-End Solutions for Your Success</h3>
                        <p className="text-lg text-stone-700 text-center mb-10 max-w-4xl mx-auto">
                            DigiEnd offers a full spectrum of digital marketing services designed to cover every aspect of your
                            online presence, from initial strategy to final conversion.
                        </p>

                        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                            {/* Service 1: Sales & Lead Generation */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=Sales" alt="Sales Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Sales & Lead Generation</h4>
                                <p className="text-lg text-stone-700">
                                    We implement sophisticated funnels and targeted campaigns to consistently generate high-quality
                                    leads and drive direct sales for your business.
                                </p>
                            </div>
                            {/* Service 2: Branding & Awareness */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=Brand" alt="Branding Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Branding & Awareness</h4>
                                <p className="text-lg text-stone-700">
                                    Build a strong, recognizable brand identity and increase your market presence with strategic
                                    awareness campaigns across various platforms.
                                </p>
                            </div>
                            {/* Service 3: Google Ads Management */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=GAds" alt="Google Ads Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Google Ads Management</h4>
                                <p className="text-lg text-stone-700">
                                    Expert setup, optimization, and daily management of Google Search, Display, Shopping, and App campaigns.
                                </p>
                            </div>
                            {/* Service 4: Meta Ads Management */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=MAds" alt="Meta Ads Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Meta Ads Management</h4>
                                <p className="text-lg text-stone-700">
                                    Targeted advertising on Facebook and Instagram to reach your precise audience, drive engagement, and conversions.
                                </p>
                            </div>
                            {/* Service 5: YouTube Promotions */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=YT" alt="YouTube Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">YouTube Promotions</h4>
                                <p className="text-lg text-stone-700">
                                    Leverage the power of video with effective YouTube ad campaigns for brand visibility and audience engagement.
                                </p>
                            </div>
                            {/* Service 6: Tag Implementations & Analytics */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=Tags" alt="Tags Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Tag Implementations & Analytics</h4>
                                <p className="text-lg text-stone-700">
                                    Accurate tracking and data insights with expert tag setup (Google Tag Manager, etc.) for informed decision-making.
                                </p>
                            </div>
                            {/* Service 7: Content Strategy & Creation */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=Content" alt="Content Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">Content Strategy & Creation</h4>
                                <p className="text-lg text-stone-700">
                                    Developing compelling content that resonates with your audience and supports your marketing goals.
                                </p>
                            </div>
                            {/* Service 8: SEO & Organic Growth */}
                            <div className="bg-blue-50 p-6 rounded-2xl shadow-lg transform hover:scale-105 transition duration-300">
                                <img src="https://placehold.co/100x100/BFE0F7/0A2C59?text=SEO" alt="SEO Icon" className="mx-auto mb-6 rounded-full"/>
                                <h4 className="text-2xl font-semibold text-blue-800 mb-3">SEO & Organic Growth</h4>
                                <p className="text-lg text-stone-700">
                                    Improving your search engine rankings and driving organic traffic through comprehensive SEO strategies.
                                </p>
                            </div>
                        </div>
                    </section>
                </div>
            </div>
        );
    };

    // Contact Us Page Component
    const ContactUsPage = () => {
        const [formData, setFormData] = useState({
            name: '',
            email: '',
            phone: '',
            company: '',
            message: '',
        });
        const [submitStatus, setSubmitStatus] = useState(''); // To show success/error message

        // Handle form input changes
        const handleChange = (e) => {
            const { name, value } = e.target;
            setFormData(prevData => ({
                ...prevData,
                [name]: value
            }));
        };

        // Handle form submission
        const handleSubmit = (e) => {
            e.preventDefault();
            // In a real application, you would send this data to a backend server.
            // For this example, we'll just log it and show a success message.
            console.log('Form Submitted:', formData);
            setSubmitStatus('Thank you for your inquiry! We will get back to you shortly.');
            setFormData({ name: '', email: '', phone: '', company: '', message: '' }); // Clear form
            setTimeout(() => setSubmitStatus(''), 5000); // Clear message after 5 seconds
        };

        return (
            <div className="pt-24 pb-8 bg-gradient-to-br from-beige-light to-blue-light text-stone-800">
                <div className="container mx-auto px-6">
                    <h2 className="text-5xl font-extrabold text-blue-800 text-center mb-12">Contact DigiEnd</h2>

                    <section className="bg-stone-100 rounded-2xl shadow-xl p-8 mb-12 max-w-3xl mx-auto">
                        <h3 className="text-3xl font-bold text-blue-700 mb-6 text-center">Get in Touch with Our Experts</h3>
                        <p className="text-lg text-stone-700 text-center mb-8">
                            Have questions or ready to start your digital marketing journey? Fill out the form below,
                            and our team will connect with you soon!
                        </p>

                        <form onSubmit={handleSubmit} className="space-y-6">
                            {/* Name Input */}
                            <div>
                                <label htmlFor="name" className="block text-lg font-medium text-stone-700 mb-2">
                                    Your Name <span className="text-red-500">*</span>
                                </label>
                                <input
                                    type="text"
                                    id="name"
                                    name="name"
                                    value={formData.name}
                                    onChange={handleChange}
                                    required
                                    className="w-full px-4 py-3 rounded-lg border-2 border-blue-200 focus:border-blue-500 focus:ring focus:ring-blue-200 transition duration-200 text-stone-800 bg-white"
                                    placeholder="Enter your name"
                                />
                            </div>
                            {/* Email Input */}
                            <div>
                                <label htmlFor="email" className="block text-lg font-medium text-stone-700 mb-2">
                                    Your Email <span className="text-red-500">*</span>
                                </label>
                                <input
                                    type="email"
                                    id="email"
                                    name="email"
                                    value={formData.email}
                                    onChange={handleChange}
                                    required
                                    className="w-full px-4 py-3 rounded-lg border-2 border-blue-200 focus:border-blue-500 focus:ring focus:ring-blue-200 transition duration-200 text-stone-800 bg-white"
                                    placeholder="Enter your email"
                                />
                            </div>
                            {/* Phone Input */}
                            <div>
                                <label htmlFor="phone" className="block text-lg font-medium text-stone-700 mb-2">
                                    Phone Number
                                </label>
                                <input
                                    type="tel"
                                    id="phone"
                                    name="phone"
                                    value={formData.phone}
                                    onChange={handleChange}
                                    className="w-full px-4 py-3 rounded-lg border-2 border-blue-200 focus:border-blue-500 focus:ring focus:ring-blue-200 transition duration-200 text-stone-800 bg-white"
                                    placeholder="e.g., +919899123876"
                                />
                            </div>
                            {/* Company Input */}
                            <div>
                                <label htmlFor="company" className="block text-lg font-medium text-stone-700 mb-2">
                                    Company Name
                                </label>
                                <input
                                    type="text"
                                    id="company"
                                    name="company"
                                    value={formData.company}
                                    onChange={handleChange}
                                    className="w-full px-4 py-3 rounded-lg border-2 border-blue-200 focus:border-blue-500 focus:ring focus:ring-blue-200 transition duration-200 text-stone-800 bg-white"
                                    placeholder="Enter your company name (optional)"
                                />
                            </div>
                            {/* Message Textarea */}
                            <div>
                                <label htmlFor="message" className="block text-lg font-medium text-stone-700 mb-2">
                                    Your Message <span className="text-red-500">*</span>
                                </label>
                                <textarea
                                    id="message"
                                    name="message"
                                    value={formData.message}
                                    onChange={handleChange}
                                    required
                                    rows="6"
                                    className="w-full px-4 py-3 rounded-lg border-2 border-blue-200 focus:border-blue-500 focus:ring focus:ring-blue-200 transition duration-200 text-stone-800 bg-white"
                                    placeholder="Tell us about your digital marketing needs..."
                                ></textarea>
                            </div>
                            {/* Submit Button */}
                            <button
                                type="submit"
                                className="w-full bg-blue-600 text-white font-bold py-3 px-6 rounded-lg text-xl shadow-lg hover:bg-blue-700 transform hover:scale-105 transition duration-300"
                            >
                                Send Message
                            </button>
                            {/* Submission Status Message */}
                            {submitStatus && (
                                <p className="mt-4 text-center text-lg font-semibold text-green-700">
                                    {submitStatus}
                                </p>
                            )}
                        </form>
                    </section>

                    {/* Contact Info Section */}
                    <section className="bg-blue-50 rounded-2xl shadow-xl p-8 max-w-3xl mx-auto text-center">
                        <h3 className="text-3xl font-bold text-blue-700 mb-6">Connect Directly</h3>
                        <p className="text-lg text-stone-700 mb-4">
                            Prefer to speak with us directly?
                        </p>
                        <div className="flex flex-col md:flex-row justify-center items-center gap-6">
                            <div className="flex items-center text-xl text-blue-800">
                                <span className="mr-2">&#9990;</span> {/* Phone icon */}
                                <a href="tel:+919899123876" className="hover:underline">+91 9899123876</a>
                            </div>
                            {/* Removed Email Address */}
                        </div>
                        <p className="text-lg text-stone-700 mt-6">
                            Our team is available Monday to Friday, 9 AM to 6 PM (Your Time Zone).
                        </p>
                    </section>
                </div>
            </div>
        );
    };

    // Tailwind CSS Configuration (added directly for demonstration)
    // In a real project, this would be in a tailwind.config.js file.
    const tailwindConfigScript = `
        <script src="https://cdn.tailwindcss.com"></script>
        <script>
            tailwind.config = {
                theme: {
                    extend: {
                        colors: {
                            'beige-light': '#F8F4EC', // Custom beige for background
                            'blue-light': '#E6F4F7',  // Custom light blue for background gradient
                            'stone-100': '#F5F5F4',
                            'stone-700': '#44403C',
                            'stone-800': '#292524',
                            'blue-50': '#EFF6FF',
                            'blue-200': '#BFDBFE',
                            'blue-500': '#3B82F6',
                            'blue-600': '#2563EB',
                            'blue-700': '#1D4ED8',
                            'blue-800': '#1E40AF',
                        },
                        fontFamily: {
                            sans: ['Inter', 'sans-serif'],
                        },
                    }
                }
            }
        </script>
        <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    `;

    // Render the appropriate page based on currentPage state
    const renderPage = () => {
        switch (currentPage) {
            case 'home':
                return <HomePage />;
            case 'about':
                return <AboutUsPage />;
            case 'services':
                return <ServicesPage />;
            case 'contact':
                return <ContactUsPage />;
            default:
                return <HomePage />; // Fallback to home
        }
    };

    return (
        <>
            {/* Inject Tailwind CSS config and font link */}
            <div dangerouslySetInnerHTML={{ __html: tailwindConfigScript }} />
            <div className="min-h-screen flex flex-col font-sans">
                <Header navigateTo={navigateTo} />
                <main className="flex-grow">
                    {renderPage()}
                </main>
                <Footer />
            </div>
        </>
    );
};

export default App;
