import React, { useState, useMemo, useEffect } from 'react';
import {
  Home,
  Flame,
  Compass,
  Clock,
  Bookmark,
  Plus,
  Bell,
  Search,
  MessageSquare,
  Share2,
  MoreHorizontal,
  ChevronUp,
  ChevronDown,
  TrendingUp,
  Users,
  Check,
  X,
  Code,
  Sparkles,
  ExternalLink,
  MessageCircle,
  ThumbsUp,
  Send,
  HelpCircle,
  Shield,
  FileText,
  Info,
  SlidersHorizontal,
  CheckCircle2,
  Menu,
  ArrowUpRight
} from 'lucide-react';

// --- INITIAL MOCK DATA ---

const INITIAL_COMMUNITIES = [
  { id: 'c1', name: 't/frontend', members: '142k', joined: true, iconBg: 'bg-blue-500', description: 'Web performance, UI engineering, CSS, and modern framework discussions.' },
  { id: 'c2', name: 't/systemdesign', members: '98k', joined: true, iconBg: 'bg-indigo-600', description: 'Architecture, distributed systems, scalability, and databases.' },
  { id: 'c3', name: 't/designsystems', members: '64k', joined: false, iconBg: 'bg-sky-500', description: 'Figma, design tokens, component architecture, and UI/UX craftsmanship.' },
  { id: 'c4', name: 't/indiehackers', members: '115k', joined: false, iconBg: 'bg-amber-500', description: 'Building products in public, revenue milestones, and SaaS growth.' },
  { id: 'c5', name: 't/ai-research', members: '210k', joined: true, iconBg: 'bg-emerald-600', description: 'LLMs, vector databases, local model fine-tuning, and AI tooling.' }
];

const INITIAL_POSTS = [
  {
    id: 'p1',
    community: 't/frontend',
    author: 'alex_dev',
    avatar: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150&auto=format&fit=crop&q=80',
    timeAgo: '2 hours ago',
    title: 'Why web component reactivity primitives are shifting back toward fine-grained signals in 2026',
    content: 'Over the last few years we saw Virtual DOM abstractions dominate the conversation. However, as browser DOM engines get faster and web applications demand lower memory footprints, fine-grained signal structures (similar to Solid signals or Vue reactivity) are becoming the preferred pattern even inside standard React/Next architectures.',
    type: 'discussion',
    tags: ['Architecture', 'JavaScript', 'WebDev'],
    upvotes: 428,
    userVote: 1, // 1 for upvoted, -1 for downvoted, 0 for neutral
    saved: false,
    comments: [
      { id: 'cm1', author: 'sarah_ui', timeAgo: '1 hour ago', content: 'Couldn’t agree more. Fine-grained reactivity drastically reduces layout shifts when handling complex real-time WebSocket feeds.', upvotes: 34 },
      { id: 'cm2', author: 'marc_k', timeAgo: '45 mins ago', content: 'What are your thoughts on compiler-driven reactivity like React Forget / React Compiler vs manual signal primitives?', upvotes: 12 }
    ],
    codeSnippet: `// Signal primitive pattern benchmark
const count = signal(0);
effect(() => {
  console.log("Count changed:", count.value);
});`
  },
  {
    id: 'p2',
    community: 't/designsystems',
    author: 'elena_design',
    avatar: 'https://images.unsplash.com/photo-1517841905240-472988babdf9?w=150&auto=format&fit=crop&q=80',
    timeAgo: '4 hours ago',
    title: 'Showcase: Modern color tokens using OKLCH for predictable visual hierarchy',
    content: 'We just migrated our entire multi-theme design system to OKLCH color space. The primary benefit is absolute lightness consistency across hues—our Electric Blue primary (#155EEF) scales into light-mode hover backgrounds (#EAF1FF) and dark contrast states without manual HEX tweaking.',
    type: 'media',
    mediaUrl: 'https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?w=1000&auto=format&fit=crop&q=80',
    tags: ['UI/UX', 'ColorTheory', 'Tailwind'],
    upvotes: 892,
    userVote: 0,
    saved: true,
    comments: [
      { id: 'cm3', author: 'brand_guru', timeAgo: '3 hours ago', content: 'OKLCH changed how we structure palette generator tools in Figma. Glad to see more platforms adopting it natively!', upvotes: 45 }
    ]
  },
  {
    id: 'p3',
    community: 't/ai-research',
    author: 'dr_quantum',
    avatar: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=150&auto=format&fit=crop&q=80',
    timeAgo: '6 hours ago',
    title: 'Community Poll: What is your primary LLM inference runtime for local edge deployment?',
    content: 'We are evaluating lightweight execution engines for running 7B to 14B parameter models directly on client hardware with WebGPU hardware acceleration.',
    type: 'poll',
    pollOptions: [
      { id: 'opt1', text: 'Ollama / llama.cpp', votes: 624 },
      { id: 'opt2', text: 'ONNX Runtime WebGPU', votes: 312 },
      { id: 'opt3', text: 'vLLM / TensorRT-LLM', votes: 418 },
      { id: 'opt4', text: 'Apple MLX framework', votes: 195 }
    ],
    pollVotedOption: 'opt1',
    tags: ['AI', 'LocalLLM', 'Performance'],
    upvotes: 310,
    userVote: 0,
    saved: false,
    comments: []
  },
  {
    id: 'p4',
    community: 't/indiehackers',
    author: 'build_in_public',
    avatar: 'https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=150&auto=format&fit=crop&q=80',
    timeAgo: '12 hours ago',
    title: 'How we hit $10k MRR in 90 days with zero paid ad spend (Community & Content First)',
    content: 'When launching our SaaS, we decided to avoid Google & Meta ads entirely. Instead, we focused on high-utility open-source tools, interactive calculators, and active participation in engineering forums like Tidderly. Here is a teardown of what worked and what flopped.',
    type: 'discussion',
    tags: ['Bootstrap', 'SaaS', 'Marketing'],
    upvotes: 1140,
    userVote: 1,
    saved: false,
    comments: [
      { id: 'cm4', author: 'founder_jay', timeAgo: '8 hours ago', content: 'Quality community engagement beats ad copy every single time. Great write-up!', upvotes: 88 }
    ]
  }
];

const TRENDING_DISCUSSIONS = [
  { id: 't1', title: 'PostgreSQL 17 performance benchmarks released', community: 't/systemdesign', engagement: '1.8k views' },
  { id: 't2', title: 'Is Tailwind CSS v4 replacing traditional CSS modules for good?', community: 't/frontend', engagement: '940 views' },
  { id: 't3', title: 'Best practices for handling offline sync in PWAs', community: 't/webdev', engagement: '620 views' }
];

const NOTIFICATIONS = [
  { id: 'n1', title: 'New reply from sarah_ui', detail: 'In "Why web component reactivity primitives..."', time: '10m ago', unread: true },
  { id: 'n2', title: 'Your post reached 400 upvotes!', detail: 't/frontend community spotlight', time: '1h ago', unread: true },
  { id: 'n3', title: 'dr_quantum started a new poll', detail: 't/ai-research', time: '5h ago', unread: false }
];

export default function App() {
  // Navigation & Search State
  const [activeTab, setActiveTab] = useState('Home'); // Home, Popular, Discover, Recent, Saved
  const [selectedFeedFilter, setSelectedFeedFilter] = useState('For You'); // For You, Popular, Latest
  const [searchQuery, setSearchQuery] = useState('');
  
  // Data State
  const [posts, setPosts] = useState(INITIAL_POSTS);
  const [communities, setCommunities] = useState(INITIAL_COMMUNITIES);
  const [notifications, setNotifications] = useState(NOTIFICATIONS);

  // Modals & Drawers
  const [isCreateModalOpen, setIsCreateModalOpen] = useState(false);
  const [activeCommentDrawerPostId, setActiveCommentDrawerPostId] = useState(null);
  const [isNotificationOpen, setIsNotificationOpen] = useState(false);
  const [isProfileMenuOpen, setIsProfileMenuOpen] = useState(false);
  
  // Toasts / Feedback
  const [toastMessage, setToastMessage] = useState('');

  const triggerToast = (msg) => {
    setToastMessage(msg);
    setTimeout(() => setToastMessage(''), 3000);
  };

  // --- HANDLERS ---

  const handleVote = (postId, direction) => {
    setPosts(prev => prev.map(p => {
      if (p.id !== postId) return p;
      let newVote = p.userVote === direction ? 0 : direction;
      let diff = newVote - p.userVote;
      return {
        ...p,
        userVote: newVote,
        upvotes: p.upvotes + diff
      };
    }));
  };

  const handleToggleSave = (postId) => {
    setPosts(prev => prev.map(p => {
      if (p.id !== postId) return p;
      const nextSaved = !p.saved;
      triggerToast(nextSaved ? 'Post saved to your bookmarks' : 'Post removed from bookmarks');
      return { ...p, saved: nextSaved };
    }));
  };

  const handleToggleCommunityJoin = (commId) => {
    setCommunities(prev => prev.map(c => {
      if (c.id !== commId) return c;
      const nextJoined = !c.joined;
      triggerToast(nextJoined ? `Joined ${c.name}` : `Left ${c.name}`);
      return { ...c, joined: nextJoined };
    }));
  };

  const handleShare = (post) => {
    const url = window.location.href;
    if (navigator.clipboard) {
      navigator.clipboard.writeText(`${url}#post-${post.id}`);
      triggerToast('Link copied to clipboard!');
    } else {
      triggerToast('Sharing link prepared!');
    }
  };

  const handlePollVote = (postId, optionId) => {
    setPosts(prev => prev.map(p => {
      if (p.id !== postId || !p.pollOptions) return p;
      if (p.pollVotedOption) return p; // prevent double vote
      const updatedOptions = p.pollOptions.map(opt => 
        opt.id === optionId ? { ...opt, votes: opt.votes + 1 } : opt
      );
      return { ...p, pollOptions: updatedOptions, pollVotedOption: optionId };
    }));
    triggerToast('Vote recorded!');
  };

  const handleAddComment = (postId, text) => {
    if (!text.trim()) return;
    const newComment = {
      id: `cm_${Date.now()}`,
      author: 'you_dev',
      timeAgo: 'Just now',
      content: text,
      upvotes: 1
    };
    setPosts(prev => prev.map(p => {
      if (p.id !== postId) return p;
      return { ...p, comments: [newComment, ...p.comments] };
    }));
    triggerToast('Comment added!');
  };

  const handleCreatePostSubmit = (newPostData) => {
    const createdPost = {
      id: `p_${Date.now()}`,
      author: 'you_dev',
      avatar: 'https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=150&auto=format&fit=crop&q=80',
      timeAgo: 'Just now',
      upvotes: 1,
      userVote: 1,
      saved: false,
      comments: [],
      ...newPostData
    };
    setPosts([createdPost, ...posts]);
    setIsCreateModalOpen(false);
    triggerToast('Discussion posted successfully!');
  };

  // --- FILTERED POSTS COMPUTATION ---

  const filteredPosts = useMemo(() => {
    return posts.filter(post => {
      // Search term filter
      if (searchQuery.trim()) {
        const query = searchQuery.toLowerCase();
        const matchesTitle = post.title.toLowerCase().includes(query);
        const matchesContent = post.content.toLowerCase().includes(query);
        const matchesCommunity = post.community.toLowerCase().includes(query);
        const matchesTag = post.tags?.some(t => t.toLowerCase().includes(query));
        if (!matchesTitle && !matchesContent && !matchesCommunity && !matchesTag) {
          return false;
        }
      }

      // Tab filter
      if (activeTab === 'Saved') {
        return post.saved;
      }

      return true;
    }).sort((a, b) => {
      if (selectedFeedFilter === 'Popular') {
        return b.upvotes - a.upvotes;
      }
      if (selectedFeedFilter === 'Latest') {
        return b.id.localeCompare(a.id);
      }
      return 0; // 'For You' default
    });
  }, [posts, searchQuery, activeTab, selectedFeedFilter]);

  const unreadCount = notifications.filter(n => n.unread).length;

  return (
    <div className="min-h-screen bg-[#F5F7FB] text-[#071B49] font-sans antialiased selection:bg-[#EAF1FF] selection:text-[#155EEF]">
      {/* Toast Notification */}
      {toastMessage && (
        <div className="fixed bottom-5 right-5 z-50 flex items-center gap-2 bg-[#071B49] text-white px-4 py-3 rounded-lg shadow-xl text-sm font-medium animate-fade-in border border-slate-700">
          <CheckCircle2 className="w-4 h-4 text-[#155EEF]" />
          <span>{toastMessage}</span>
        </div>
      )}

      {/* TOP STICKY NAVIGATION BAR */}
      <header className="sticky top-0 z-40 bg-white border-b border-slate-200 shadow-sm">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between gap-4">
          
          {/* Brand Logo & Name */}
          <div className="flex items-center gap-3 min-w-fit">
            <button 
              onClick={() => { setActiveTab('Home'); setSearchQuery(''); }}
              className="flex items-center gap-2.5 focus:outline-none group"
            >
              {/* Custom SVG Logo Icon */}
              <div className="w-9 h-9 rounded-xl bg-[#155EEF] flex items-center justify-center text-white shadow-md group-hover:bg-blue-700 transition-colors">
                <svg className="w-5 h-5 fill-current" viewBox="0 0 24 24">
                  <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 14.5v-9l6 4.5-6 4.5z" />
                </svg>
              </div>
              <span className="text-xl font-bold tracking-tight text-[#071B49] flex items-center gap-1">
                Tidderly
                <span className="w-2 h-2 rounded-full bg-[#155EEF] inline-block"></span>
              </span>
            </button>
          </div>

          {/* Central Search Field */}
          <div className="flex-1 max-w-2xl mx-2 hidden sm:block">
            <div className="relative">
              <Search className="absolute left-3.5 top-1/2 -translate-y-1/2 w-4 h-4 text-[#64748B]" />
              <input
                type="text"
                value={searchQuery}
                onChange={(e) => setSearchQuery(e.target.value)}
                placeholder="Search discussions, communities, tags, and people..."
                className="w-full pl-10 pr-10 py-2 bg-[#F5F7FB] border border-slate-200 rounded-full text-sm text-[#071B49] placeholder-[#64748B] focus:outline-none focus:ring-2 focus:ring-[#155EEF]/20 focus:border-[#155EEF] transition-all"
              />
              {searchQuery && (
                <button 
                  onClick={() => setSearchQuery('')}
                  className="absolute right-3 top-1/2 -translate-y-1/2 text-[#64748B] hover:text-[#071B49] p-0.5 rounded-full"
                >
                  <X className="w-4 h-4" />
                </button>
              )}
            </div>
          </div>

          {/* Right Action Menu */}
          <div className="flex items-center gap-3">
            {/* Create Post Action Button */}
            <button
              onClick={() => setIsCreateModalOpen(true)}
              className="flex items-center gap-2 bg-[#155EEF] hover:bg-blue-700 text-white font-medium px-4 py-2 rounded-lg text-sm transition-all shadow-sm active:scale-[0.98]"
            >
              <Plus className="w-4 h-4" />
              <span className="hidden sm:inline">Create Post</span>
            </button>

            {/* Notification Bell Dropdown Toggle */}
            <div className="relative">
              <button
                onClick={() => { setIsNotificationOpen(!isNotificationOpen); setIsProfileMenuOpen(false); }}
                className="relative p-2 text-[#64748B] hover:text-[#071B49] hover:bg-[#F5F7FB] rounded-lg transition-colors focus:outline-none"
                aria-label="Notifications"
              >
                <Bell className="w-5 h-5" />
                {unreadCount > 0 && (
                  <span className="absolute top-1.5 right-1.5 w-2 h-2 rounded-full bg-[#155EEF] ring-2 ring-white" />
                )}
              </button>

              {/* Notifications Popover */}
              {isNotificationOpen && (
                <div className="absolute right-0 mt-2 w-80 sm:w-96 bg-white rounded-xl shadow-xl border border-slate-200 py-2 z-50 animate-in fade-in slide-in-from-top-2">
                  <div className="px-4 py-2 border-b border-slate-100 flex items-center justify-between">
                    <span className="font-semibold text-sm text-[#071B49]">Notifications</span>
                    <button 
                      onClick={() => setNotifications(notifications.map(n => ({ ...n, unread: false })))}
                      className="text-xs text-[#155EEF] hover:underline"
                    >
                      Mark all as read
                    </button>
                  </div>
                  <div className="max-h-80 overflow-y-auto divide-y divide-slate-100">
                    {notifications.map(n => (
                      <div key={n.id} className={`p-3.5 hover:bg-[#F5F7FB] transition-colors cursor-pointer ${n.unread ? 'bg-[#EAF1FF]/40' : ''}`}>
                        <p className="text-xs font-semibold text-[#071B49]">{n.title}</p>
                        <p className="text-xs text-[#64748B] mt-0.5">{n.detail}</p>
                        <span className="text-[10px] text-slate-400 mt-1 block">{n.time}</span>
                      </div>
                    ))}
                  </div>
                </div>
              )}
            </div>

            {/* User Profile Dropdown Toggle */}
            <div className="relative">
              <button
                onClick={() => { setIsProfileMenuOpen(!isProfileMenuOpen); setIsNotificationOpen(false); }}
                className="flex items-center gap-2 p-1 rounded-full hover:bg-slate-100 focus:outline-none transition-colors"
              >
                <img
                  src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=150&auto=format&fit=crop&q=80"
                  alt="User avatar"
                  className="w-8 h-8 rounded-full border border-slate-200 object-cover"
                />
              </button>

              {/* Profile Menu Popover */}
              {isProfileMenuOpen && (
                <div className="absolute right-0 mt-2 w-56 bg-white rounded-xl shadow-xl border border-slate-200 py-2 z-50 text-sm">
                  <div className="px-4 py-2.5 border-b border-slate-100">
                    <p className="font-semibold text-[#071B49]">you_dev</p>
                    <p className="text-xs text-[#64748B]">alex.dev@tidderly.com</p>
                  </div>
                  <div className="py-1">
                    <button onClick={() => { setActiveTab('Saved'); setIsProfileMenuOpen(false); }} className="w-full text-left px-4 py-2 text-[#071B49] hover:bg-[#EAF1FF] flex items-center gap-2">
                      <Bookmark className="w-4 h-4 text-[#64748B]" />
                      Saved Posts
                    </button>
                    <button className="w-full text-left px-4 py-2 text-[#071B49] hover:bg-[#EAF1FF] flex items-center gap-2">
                      <SlidersHorizontal className="w-4 h-4 text-[#64748B]" />
                      Preferences
                    </button>
                  </div>
                  <div className="border-t border-slate-100 pt-1">
                    <button className="w-full text-left px-4 py-2 text-red-600 hover:bg-red-50 flex items-center gap-2">
                      Sign Out
                    </button>
                  </div>
                </div>
              )}
            </div>

          </div>
        </div>

        {/* Mobile Search Input Bar */}
        <div className="sm:hidden px-4 pb-3">
          <div className="relative">
            <Search className="absolute left-3.5 top-1/2 -translate-y-1/2 w-4 h-4 text-[#64748B]" />
            <input
              type="text"
              value={searchQuery}
              onChange={(e) => setSearchQuery(e.target.value)}
              placeholder="Search discussions..."
              className="w-full pl-10 pr-8 py-1.5 bg-[#F5F7FB] border border-slate-200 rounded-full text-xs text-[#071B49]"
            />
          </div>
        </div>
      </header>

      {/* MAIN CONTAINER (THREE-COLUMN DESKTOP LAYOUT) */}
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
          
          {/* ==================== LEFT SIDEBAR ==================== */}
          <aside className="hidden lg:block lg:col-span-3 sticky top-22 space-y-6">
            
            {/* Primary Navigation Links */}
            <div className="bg-white rounded-xl p-3 border border-slate-200 shadow-sm space-y-1">
              {[
                { name: 'Home', icon: Home },
                { name: 'Popular', icon: Flame },
                { name: 'Discover', icon: Compass },
                { name: 'Recent', icon: Clock },
                { name: 'Saved', icon: Bookmark, badge: posts.filter(p => p.saved).length }
              ].map(item => {
                const Icon = item.icon;
                const isActive = activeTab === item.name;
                return (
                  <button
                    key={item.name}
                    onClick={() => setActiveTab(item.name)}
                    className={`w-full flex items-center justify-between px-3.5 py-2.5 rounded-lg text-sm font-medium transition-colors ${
                      isActive 
                        ? 'bg-[#EAF1FF] text-[#155EEF]' 
                        : 'text-[#071B49] hover:bg-[#F5F7FB] hover:text-[#155EEF]'
                    }`}
                  >
                    <div className="flex items-center gap-3">
                      <Icon className={`w-4 h-4 ${isActive ? 'text-[#155EEF]' : 'text-[#64748B]'}`} />
                      <span>{item.name}</span>
                    </div>
                    {item.badge !== undefined && item.badge > 0 && (
                      <span className="bg-[#155EEF] text-white text-[11px] font-semibold px-2 py-0.5 rounded-full">
                        {item.badge}
                      </span>
                    )}
                  </button>
                );
              })}
            </div>

            {/* Your Communities Section */}
            <div className="bg-white rounded-xl p-4 border border-slate-200 shadow-sm space-y-3">
              <div className="flex items-center justify-between text-xs font-bold text-[#64748B] uppercase tracking-wider px-1">
                <span>Your Communities</span>
                <Users className="w-3.5 h-3.5" />
              </div>

              <div className="space-y-1">
                {communities.map(comm => (
                  <div
                    key={comm.id}
                    className="flex items-center justify-between p-2 rounded-lg hover:bg-[#F5F7FB] transition-colors group cursor-pointer"
                    onClick={() => setSearchQuery(comm.name)}
                  >
                    <div className="flex items-center gap-2.5 overflow-hidden">
                      <div className={`w-7 h-7 rounded-md ${comm.iconBg} text-white flex items-center justify-center font-bold text-xs shrink-0`}>
                        {comm.name.charAt(2).toUpperCase()}
                      </div>
                      <div className="truncate">
                        <p className="text-xs font-semibold text-[#071B49] truncate group-hover:text-[#155EEF] transition-colors">{comm.name}</p>
                        <p className="text-[11px] text-[#64748B]">{comm.members} members</p>
                      </div>
                    </div>
                    <button
                      onClick={(e) => { e.stopPropagation(); handleToggleCommunityJoin(comm.id); }}
                      className={`text-xs px-2.5 py-1 rounded-md font-medium transition-all ${
                        comm.joined 
                          ? 'bg-slate-100 text-slate-600 hover:bg-slate-200' 
                          : 'bg-[#EAF1FF] text-[#155EEF] hover:bg-blue-100'
                      }`}
                    >
                      {comm.joined ? 'Joined' : 'Join'}
                    </button>
                  </div>
                ))}
              </div>

              <button
                onClick={() => setActiveTab('Discover')}
                className="w-full mt-2 text-center text-xs font-semibold text-[#155EEF] hover:underline py-1"
              >
                Discover More Communities →
              </button>
            </div>

            {/* Quick Stats or Platform Note */}
            <div className="bg-[#EAF1FF]/60 rounded-xl p-4 border border-[#155EEF]/10 text-xs text-[#071B49] space-y-1">
              <p className="font-semibold flex items-center gap-1.5 text-[#155EEF]">
                <Sparkles className="w-3.5 h-3.5" /> Tidderly Daily Digest
              </p>
              <p className="text-[#64748B] leading-relaxed">
                Connect with developers, designers, and researchers in curated, moderated spaces.
              </p>
            </div>

          </aside>

          {/* ==================== CENTER MAIN FEED ==================== */}
          <main className="lg:col-span-6 space-y-4">
            
            {/* Feed Context Header */}
            <div className="bg-white rounded-xl p-4 border border-slate-200 shadow-sm flex flex-col sm:flex-row sm:items-center justify-between gap-3">
              <div>
                <h1 className="text-lg font-bold text-[#071B49] tracking-tight">
                  {activeTab === 'Saved' ? 'Your Saved Bookmarks' : `${activeTab} Discussions`}
                </h1>
                <p className="text-xs text-[#64748B] mt-0.5">
                  {searchQuery 
                    ? `Showing results matching "${searchQuery}"` 
                    : 'Explore high quality discussions from communities you follow'}
                </p>
              </div>

              {/* Feed Filter Segmented Controls */}
              <div className="flex items-center gap-1 bg-[#F5F7FB] p-1 rounded-lg border border-slate-200 self-start sm:self-auto">
                {['For You', 'Popular', 'Latest'].map(filter => (
                  <button
                    key={filter}
                    onClick={() => setSelectedFeedFilter(filter)}
                    className={`px-3 py-1 rounded-md text-xs font-medium transition-all ${
                      selectedFeedFilter === filter
                        ? 'bg-white text-[#155EEF] shadow-sm font-semibold'
                        : 'text-[#64748B] hover:text-[#071B49]'
                    }`}
                  >
                    {filter}
                  </button>
                ))}
              </div>
            </div>

            {/* Interactive Post Creation Prompt */}
            <div className="bg-white rounded-xl p-4 border border-slate-200 shadow-sm flex items-center gap-3">
              <img
                src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=150&auto=format&fit=crop&q=80"
                alt="Your avatar"
                className="w-9 h-9 rounded-full object-cover border border-slate-200 shrink-0"
              />
              <button
                onClick={() => setIsCreateModalOpen(true)}
                className="flex-1 text-left bg-[#F5F7FB] hover:bg-[#EAF1FF]/50 border border-slate-200 rounded-lg px-4 py-2.5 text-xs text-[#64748B] transition-colors flex items-center justify-between group"
              >
                <span>Start a discussion or ask a question...</span>
                <Plus className="w-4 h-4 text-[#155EEF] group-hover:scale-110 transition-transform" />
              </button>
            </div>

            {/* Post Feed List */}
            {filteredPosts.length === 0 ? (
              <div className="bg-white rounded-xl p-12 text-center border border-slate-200 shadow-sm space-y-3">
                <div className="w-12 h-12 bg-slate-100 rounded-full flex items-center justify-center mx-auto text-[#64748B]">
                  <MessageSquare className="w-6 h-6" />
                </div>
                <h3 className="text-base font-semibold text-[#071B49]">No discussions found</h3>
                <p className="text-xs text-[#64748B] max-w-sm mx-auto">
                  We couldn't find any posts matching your criteria. Try adjusting your search query or create a new discussion.
                </p>
                <button
                  onClick={() => { setSearchQuery(''); setActiveTab('Home'); }}
                  className="mt-2 text-xs text-[#155EEF] font-semibold hover:underline"
                >
                  Reset all filters
                </button>
              </div>
            ) : (
              filteredPosts.map(post => (
                <article
                  key={post.id}
                  className="bg-white rounded-xl border border-slate-200 shadow-sm hover:border-slate-300 transition-all overflow-hidden"
                >
                  <div className="p-4 sm:p-5">
                    
                    {/* Post Header: Community, Author & Time */}
                    <div className="flex items-center justify-between text-xs mb-2">
                      <div className="flex items-center gap-2 flex-wrap">
                        <button 
                          onClick={() => setSearchQuery(post.community)}
                          className="font-bold text-[#155EEF] hover:underline"
                        >
                          {post.community}
                        </button>
                        <span className="text-slate-300">•</span>
                        <span className="text-[#64748B]">Posted by u/{post.author}</span>
                        <span className="text-slate-300">•</span>
                        <span className="text-[#64748B]">{post.timeAgo}</span>
                      </div>

                      {/* Post Tags */}
                      <div className="flex items-center gap-1.5">
                        {post.tags?.map(tag => (
                          <span key={tag} className="bg-slate-100 text-slate-600 px-2 py-0.5 rounded text-[10px] font-medium hidden sm:inline-block">
                            #{tag}
                          </span>
                        ))}
                      </div>
                    </div>

                    {/* Post Title */}
                    <h2 className="text-base sm:text-lg font-bold text-[#071B49] leading-snug mb-2 hover:text-[#155EEF] cursor-pointer transition-colors" onClick={() => setActiveCommentDrawerPostId(post.id)}>
                      {post.title}
                    </h2>

                    {/* Post Content Excerpt */}
                    <p className="text-xs sm:text-sm text-[#071B49]/80 leading-relaxed mb-4">
                      {post.content}
                    </p>

                    {/* Optional Media Preview / Code Snippet / Poll */}
                    {post.type === 'media' && post.mediaUrl && (
                      <div className="mb-4 rounded-lg overflow-hidden border border-slate-200 bg-slate-50">
                        <img 
                          src={post.mediaUrl} 
                          alt="Post visual content" 
                          className="w-full h-auto max-h-80 object-cover"
                        />
                      </div>
                    )}

                    {post.codeSnippet && (
                      <div className="mb-4 bg-[#071B49] rounded-lg p-3 text-xs font-mono text-blue-200 overflow-x-auto relative">
                        <div className="flex items-center justify-between text-[10px] text-slate-400 border-b border-slate-700 pb-1 mb-2">
                          <span className="flex items-center gap-1"><Code className="w-3 h-3" /> Code Preview</span>
                        </div>
                        <pre><code>{post.codeSnippet}</code></pre>
                      </div>
                    )}

                    {post.type === 'poll' && post.pollOptions && (
                      <div className="mb-4 bg-[#F5F7FB] rounded-lg p-3.5 border border-slate-200 space-y-2">
                        <p className="text-xs font-semibold text-[#071B49] mb-1">Community Options:</p>
                        {post.pollOptions.map(opt => {
                          const totalVotes = post.pollOptions.reduce((acc, curr) => acc + curr.votes, 0);
                          const percentage = totalVotes > 0 ? Math.round((opt.votes / totalVotes) * 100) : 0;
                          const isVoted = post.pollVotedOption === opt.id;

                          return (
                            <button
                              key={opt.id}
                              onClick={() => handlePollVote(post.id, opt.id)}
                              disabled={!!post.pollVotedOption}
                              className={`w-full text-left p-2.5 rounded-md border text-xs relative overflow-hidden transition-all ${
                                isVoted ? 'border-[#155EEF] bg-[#EAF1FF]/40 font-medium' : 'border-slate-200 hover:border-slate-300 bg-white'
                              }`}
                            >
                              <div className="flex justify-between items-center z-10 relative">
                                <span>{opt.text}</span>
                                <span className="text-[11px] text-[#64748B] font-semibold">{percentage}% ({opt.votes})</span>
                              </div>
                              <div 
                                className="absolute left-0 top-0 bottom-0 bg-[#155EEF]/10 z-0 transition-all duration-500"
                                style={{ width: `${percentage}%` }}
                              />
                            </button>
                          );
                        })}
                      </div>
                    )}

                    {/* Interactive Action Row */}
                    <div className="flex items-center justify-between pt-3 border-t border-slate-100 text-xs font-medium text-[#64748B]">
                      
                      {/* Upvote & Downvote Control Pill */}
                      <div className="flex items-center bg-[#F5F7FB] border border-slate-200 rounded-lg overflow-hidden">
                        <button
                          onClick={() => handleVote(post.id, 1)}
                          className={`p-1.5 hover:bg-slate-200 transition-colors ${
                            post.userVote === 1 ? 'text-[#155EEF] bg-[#EAF1FF]' : ''
                          }`}
                          aria-label="Upvote"
                        >
                          <ChevronUp className="w-4 h-4" />
                        </button>
                        <span className={`px-2 font-bold text-xs ${
                          post.userVote === 1 ? 'text-[#155EEF]' : post.userVote === -1 ? 'text-red-500' : 'text-[#071B49]'
                        }`}>
                          {post.upvotes}
                        </span>
                        <button
                          onClick={() => handleVote(post.id, -1)}
                          className={`p-1.5 hover:bg-slate-200 transition-colors ${
                            post.userVote === -1 ? 'text-red-500 bg-red-50' : ''
                          }`}
                          aria-label="Downvote"
                        >
                          <ChevronDown className="w-4 h-4" />
                        </button>
                      </div>

                      {/* Comments Trigger */}
                      <button
                        onClick={() => setActiveCommentDrawerPostId(post.id)}
                        className="flex items-center gap-1.5 hover:bg-[#F5F7FB] px-2.5 py-1.5 rounded-lg transition-colors"
                      >
                        <MessageSquare className="w-4 h-4 text-[#64748B]" />
                        <span>{post.comments.length} Comments</span>
                      </button>

                      {/* Share Action */}
                      <button
                        onClick={() => handleShare(post)}
                        className="flex items-center gap-1.5 hover:bg-[#F5F7FB] px-2.5 py-1.5 rounded-lg transition-colors"
                      >
                        <Share2 className="w-4 h-4 text-[#64748B]" />
                        <span className="hidden sm:inline">Share</span>
                      </button>

                      {/* Bookmark / Save Action */}
                      <button
                        onClick={() => handleToggleSave(post.id)}
                        className={`flex items-center gap-1.5 px-2.5 py-1.5 rounded-lg transition-colors ${
                          post.saved ? 'text-[#155EEF] bg-[#EAF1FF]' : 'hover:bg-[#F5F7FB]'
                        }`}
                      >
                        <Bookmark className={`w-4 h-4 ${post.saved ? 'fill-current text-[#155EEF]' : ''}`} />
                        <span className="hidden sm:inline">{post.saved ? 'Saved' : 'Save'}</span>
                      </button>

                    </div>

                  </div>
                </article>
              ))
            )}

          </main>

          {/* ==================== RIGHT SIDEBAR ==================== */}
          <aside className="hidden lg:block lg:col-span-3 sticky top-22 space-y-6">
            
            {/* Trending Discussions Widget */}
            <div className="bg-white rounded-xl p-4 border border-slate-200 shadow-sm space-y-3">
              <div className="flex items-center gap-2 text-xs font-bold text-[#071B49] uppercase tracking-wider">
                <TrendingUp className="w-4 h-4 text-[#155EEF]" />
                <span>Trending Discussions</span>
              </div>

              <div className="space-y-3 divide-y divide-slate-100">
                {TRENDING_DISCUSSIONS.map((item, idx) => (
                  <div key={item.id} className={`${idx > 0 ? 'pt-2.5' : ''} space-y-0.5 group cursor-pointer`} onClick={() => setSearchQuery(item.title)}>
                    <p className="text-xs font-semibold text-[#071B49] group-hover:text-[#155EEF] transition-colors leading-snug">
                      {item.title}
                    </p>
                    <div className="flex items-center justify-between text-[11px] text-[#64748B]">
                      <span>{item.community}</span>
                      <span>{item.engagement}</span>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            {/* Communities to Explore Widget */}
            <div className="bg-white rounded-xl p-4 border border-slate-200 shadow-sm space-y-3">
              <div className="flex items-center justify-between text-xs font-bold text-[#071B49] uppercase tracking-wider">
                <span>Suggested Communities</span>
                <Compass className="w-4 h-4 text-[#155EEF]" />
              </div>

              <div className="space-y-3">
                {communities.filter(c => !c.joined).map(comm => (
                  <div key={comm.id} className="flex items-start justify-between gap-2">
                    <div className="space-y-0.5">
                      <p className="text-xs font-bold text-[#071B49]">{comm.name}</p>
                      <p className="text-[11px] text-[#64748B] leading-tight line-clamp-2">{comm.description}</p>
                    </div>
                    <button
                      onClick={() => handleToggleCommunityJoin(comm.id)}
                      className="text-xs bg-[#EAF1FF] text-[#155EEF] font-semibold px-2.5 py-1 rounded-md hover:bg-blue-100 shrink-0 transition-colors"
                    >
                      Join
                    </button>
                  </div>
                ))}
              </div>
            </div>

            {/* Daily Prompt Interactive Widget */}
            <div className="bg-gradient-to-br from-[#071B49] to-blue-900 rounded-xl p-4 text-white shadow-sm space-y-2">
              <span className="text-[10px] uppercase tracking-widest text-blue-300 font-semibold">Daily Community Prompt</span>
              <p className="text-xs font-medium leading-relaxed">
                "What is a tool or library you discovered this week that radically improved your workflow?"
              </p>
              <button 
                onClick={() => setIsCreateModalOpen(true)}
                className="mt-2 w-full bg-[#155EEF] hover:bg-blue-600 text-white text-xs font-medium py-1.5 px-3 rounded-lg transition-colors flex items-center justify-center gap-1.5"
              >
                <span>Share your response</span>
                <ArrowUpRight className="w-3.5 h-3.5" />
              </button>
            </div>

            {/* Clean Footer Links */}
            <footer className="px-1 text-[11px] text-[#64748B] space-y-2">
              <div className="flex flex-wrap gap-x-3 gap-y-1">
                <a href="#about" className="hover:underline">About</a>
                <a href="#guidelines" className="hover:underline">Guidelines</a>
                <a href="#privacy" className="hover:underline">Privacy Policy</a>
                <a href="#terms" className="hover:underline">Terms</a>
                <a href="#help" className="hover:underline">Help Center</a>
              </div>
              <p>© 2026 Tidderly Inc. All rights reserved.</p>
            </footer>

          </aside>

        </div>
      </div>

      {/* MOBILE BOTTOM NAVIGATION BAR */}
      <nav className="lg:hidden fixed bottom-0 left-0 right-0 bg-white border-t border-slate-200 z-30 px-3 py-2 flex items-center justify-around text-[#64748B]">
        {[
          { name: 'Home', icon: Home },
          { name: 'Popular', icon: Flame },
          { name: 'Saved', icon: Bookmark },
          { name: 'Discover', icon: Compass }
        ].map(item => {
          const Icon = item.icon;
          const isActive = activeTab === item.name;
          return (
            <button
              key={item.name}
              onClick={() => setActiveTab(item.name)}
              className={`flex flex-col items-center gap-0.5 text-[10px] font-medium ${
                isActive ? 'text-[#155EEF]' : 'hover:text-[#071B49]'
              }`}
            >
              <Icon className="w-5 h-5" />
              <span>{item.name}</span>
            </button>
          );
        })}
      </nav>

      {/* CREATE POST MODAL OVERLAY */}
      {isCreateModalOpen && (
        <div className="fixed inset-0 bg-black/50 z-50 flex items-center justify-center p-4 backdrop-blur-sm animate-in fade-in">
          <div className="bg-white rounded-2xl max-w-lg w-full p-6 shadow-2xl border border-slate-200 space-y-4">
            
            <div className="flex items-center justify-between border-b border-slate-100 pb-3">
              <h3 className="text-lg font-bold text-[#071B49]">Create a Discussion</h3>
              <button 
                onClick={() => setIsCreateModalOpen(false)}
                className="text-[#64748B] hover:text-[#071B49] p-1 rounded-lg"
              >
                <X className="w-5 h-5" />
              </button>
            </div>

            <form 
              onSubmit={(e) => {
                e.preventDefault();
                const formData = new FormData(e.target);
                handleCreatePostSubmit({
                  title: formData.get('title'),
                  content: formData.get('content'),
                  community: formData.get('community'),
                  tags: formData.get('tags')?.toString().split(',').map(t => t.trim()).filter(Boolean) || ['Discussion'],
                  type: 'discussion'
                });
              }}
              className="space-y-4"
            >
              <div>
                <label className="block text-xs font-semibold text-[#071B49] mb-1">Select Community</label>
                <select 
                  name="community"
                  className="w-full bg-[#F5F7FB] border border-slate-200 rounded-lg px-3 py-2 text-xs text-[#071B49] focus:outline-none focus:border-[#155EEF]"
                >
                  {communities.map(c => (
                    <option key={c.id} value={c.name}>{c.name}</option>
                  ))}
                </select>
              </div>

              <div>
                <label className="block text-xs font-semibold text-[#071B49] mb-1">Discussion Title</label>
                <input
                  type="text"
                  name="title"
                  required
                  placeholder="What is on your mind?"
                  className="w-full bg-[#F5F7FB] border border-slate-200 rounded-lg px-3 py-2 text-sm text-[#071B49] placeholder-[#64748B] focus:outline-none focus:border-[#155EEF]"
                />
              </div>

              <div>
                <label className="block text-xs font-semibold text-[#071B49] mb-1">Content / Body</label>
                <textarea
                  name="content"
                  required
                  rows={4}
                  placeholder="Provide context, ask a thoughtful question, or share details..."
                  className="w-full bg-[#F5F7FB] border border-slate-200 rounded-lg px-3 py-2 text-xs text-[#071B49] placeholder-[#64748B] focus:outline-none focus:border-[#155EEF]"
                />
              </div>

              <div>
                <label className="block text-xs font-semibold text-[#071B49] mb-1">Tags (Comma separated)</label>
                <input
                  type="text"
                  name="tags"
                  placeholder="WebDev, React, Design"
                  className="w-full bg-[#F5F7FB] border border-slate-200 rounded-lg px-3 py-2 text-xs text-[#071B49] focus:outline-none focus:border-[#155EEF]"
                />
              </div>

              <div className="flex justify-end gap-2 pt-2 border-t border-slate-100">
                <button
                  type="button"
                  onClick={() => setIsCreateModalOpen(false)}
                  className="px-4 py-2 rounded-lg text-xs font-semibold text-[#64748B] hover:bg-slate-100"
                >
                  Cancel
                </button>
                <button
                  type="submit"
                  className="px-5 py-2 bg-[#155EEF] hover:bg-blue-700 text-white rounded-lg text-xs font-semibold transition-all shadow-sm"
                >
                  Post Discussion
                </button>
              </div>
            </form>

          </div>
        </div>
      )}

      {/* COMMENTS DRAWER / OVERLAY */}
      {activeCommentDrawerPostId && (() => {
        const activePost = posts.find(p => p.id === activeCommentDrawerPostId);
        if (!activePost) return null;

        return (
          <div className="fixed inset-0 bg-black/40 z-50 flex justify-end backdrop-blur-xs">
            <div className="bg-white w-full max-w-lg h-full p-6 overflow-y-auto shadow-2xl flex flex-col justify-between animate-in slide-in-from-right">
              
              <div>
                <div className="flex items-center justify-between border-b border-slate-100 pb-3 mb-4">
                  <h3 className="text-base font-bold text-[#071B49]">Comments & Discussion</h3>
                  <button 
                    onClick={() => setActiveCommentDrawerPostId(null)}
                    className="text-[#64748B] hover:text-[#071B49] p-1 rounded-lg"
                  >
                    <X className="w-5 h-5" />
                  </button>
                </div>

                <div className="space-y-2 mb-6">
                  <span className="text-xs font-bold text-[#155EEF]">{activePost.community}</span>
                  <h4 className="text-sm font-bold text-[#071B49]">{activePost.title}</h4>
                  <p className="text-xs text-[#64748B] line-clamp-3">{activePost.content}</p>
                </div>

                <div className="border-t border-slate-100 pt-4 space-y-4">
                  <h5 className="text-xs font-bold text-[#071B49] uppercase tracking-wider">
                    Responses ({activePost.comments.length})
                  </h5>

                  {activePost.comments.length === 0 ? (
                    <p className="text-xs text-[#64748B] italic py-4">No comments yet. Be the first to join the conversation!</p>
                  ) : (
                    activePost.comments.map(cm => (
                      <div key={cm.id} className="bg-[#F5F7FB] p-3 rounded-lg border border-slate-200 space-y-1.5">
                        <div className="flex items-center justify-between text-[11px]">
                          <span className="font-bold text-[#071B49]">u/{cm.author}</span>
                          <span className="text-[#64748B]">{cm.timeAgo}</span>
                        </div>
                        <p className="text-xs text-[#071B49] leading-relaxed">{cm.content}</p>
                        <div className="flex items-center gap-2 text-[11px] text-[#64748B] pt-1">
                          <button className="flex items-center gap-1 hover:text-[#155EEF]">
                            <ThumbsUp className="w-3 h-3" />
                            <span>{cm.upvotes}</span>
                          </button>
                        </div>
                      </div>
                    ))
                  )}
                </div>
              </div>

              {/* Add Comment Input Footer */}
              <div className="border-t border-slate-200 pt-3 mt-4">
                <form
                  onSubmit={(e) => {
                    e.preventDefault();
                    const input = e.target.elements.commentInput;
                    handleAddComment(activePost.id, input.value);
                    input.value = '';
                  }}
                  className="flex items-center gap-2"
                >
                  <input
                    type="text"
                    name="commentInput"
                    placeholder="Write a constructive reply..."
                    className="flex-1 bg-[#F5F7FB] border border-slate-200 rounded-lg px-3 py-2 text-xs text-[#071B49] focus:outline-none focus:border-[#155EEF]"
                  />
                  <button
                    type="submit"
                    className="bg-[#155EEF] hover:bg-blue-700 text-white p-2 rounded-lg transition-colors"
                  >
                    <Send className="w-4 h-4" />
                  </button>
                </form>
              </div>

            </div>
          </div>
        );
      })()}

    </div>
  );
}
