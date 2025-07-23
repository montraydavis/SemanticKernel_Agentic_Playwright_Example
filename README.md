# Microsoft Semantic Kernel with Playwright
## AI-Powered Web Automation Agent Tutorial

> **Learn to build intelligent AI agents that autonomously control web browsers using Microsoft Semantic Kernel and Playwright for automated research and content analysis.**

<div align="center">

[![.NET 8.0](https://img.shields.io/badge/.NET-8.0-purple.svg)](https://dotnet.microsoft.com/download/dotnet/8.0)
[![Semantic Kernel](https://img.shields.io/badge/Semantic%20Kernel-1.60.0-blue.svg)](https://github.com/microsoft/semantic-kernel)
[![Playwright](https://img.shields.io/badge/Playwright-1.54.0-green.svg)](https://playwright.dev/)
[![OpenAI](https://img.shields.io/badge/OpenAI-Function%20Calling-orange.svg)](https://platform.openai.com/docs/guides/function-calling)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

</div>

---

## 🎯 What You'll Master

This comprehensive tutorial teaches you to build **autonomous AI agents** that can intelligently control web browsers to perform research tasks. You'll learn to combine the decision-making power of large language models with the precision of browser automation.

### Core Technologies
- **Microsoft Semantic Kernel**: AI orchestration and function calling framework
- **Playwright**: Cross-browser automation library for reliable web interactions
- **OpenAI Function Calling**: Automatic function selection and execution by AI
- **Agent Architecture**: Conversational AI that maintains context and adapts behavior
- **Browser Automation**: Programmatic control of web browsers for data extraction

---

## 📚 Learning Resources

### 🎧 Audio Tutorial
**[AI Web Automation with Semantic Kernel and Playwright](./Assets/sk.mp3)**
> *Perfect for understanding concepts while commuting or multitasking*

A comprehensive audio walkthrough covering the entire AI agent implementation from function calling concepts to production deployment.

### 🔬 Interactive Jupyter Notebook
**[SemanticKernel_Agents_Playwright.ipynb](./SemanticKernel_Agents_Playwright.ipynb)**
> *Hands-on learning with live code execution and browser automation*

Step-by-step implementation with running code, real browser interactions, and detailed explanations of AI function calling.

---

## 🚀 Quick Start

### Prerequisites
- **.NET 8.0 SDK** or later
- **OpenAI API Key** (for AI function calling)
- **Visual Studio Code** with .NET Interactive extension
- **Jupyter** support for .NET Interactive

### 🔧 Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/semantic-kernel-playwright-agent.git
   cd semantic-kernel-playwright-agent
   ```

2. **Set your OpenAI API key**
   ```bash
   # Windows
   set OPENAI_API_KEY=your_openai_api_key_here

   # macOS/Linux  
   export OPENAI_API_KEY=your_openai_api_key_here
   ```

3. **Choose your learning path**
   - 🎧 **Audio**: Play the [MP3 tutorial](./Assets/sk.mp3)
   - 🔬 **Interactive**: Open the [Jupyter notebook](./SemanticKernel_Agents_Playwright.ipynb)

---

## 🏗️ What You'll Build

### Intelligent Research Agent
A complete AI-powered browser automation system that demonstrates:

```csharp
// Create an AI agent that autonomously researches topics
var researchAgent = new ChatCompletionAgent()
{
    Name = "ResearchAgent",
    Instructions = """
        You are a research assistant that can search Google and analyze web content.
        
        When asked to research a topic:
        1. Launch the browser using LaunchBrowser
        2. Navigate to Google using NavigateToGoogle  
        3. Search for the requested topic using SearchFor
        4. Get the search results using GetSearchResults
        5. Visit the most relevant pages using GetPageContent
        6. Provide a comprehensive summary of your findings
        """,
    Kernel = kernel
};

// Agent automatically orchestrates browser operations
await foreach (var message in researchAgent.InvokeAsync("Research C# 12 features", thread))
{
    Console.WriteLine($"Agent: {message.Message.Content}");
}
```

### Key Features Implemented
- **🤖 Autonomous Decision Making**: AI automatically selects which browser functions to call
- **🔄 Function Calling**: Seamless integration between AI reasoning and browser automation  
- **🌐 Google Search Integration**: Automated search and result extraction
- **📄 Content Analysis**: Intelligent content extraction from web pages
- **💬 Conversational Interface**: Natural language research requests
- **🛡️ Error Recovery**: Graceful handling of browser automation failures
- **🧹 Resource Management**: Proper cleanup of browser processes

---

## 🎓 Learning Path Recommendations

### 👶 **Beginner** (New to AI agents)
1. 🎧 Listen to the audio tutorial for foundational concepts
2. 🔬 Follow notebook sections 1-5 to understand function calling
3. 🔍 Focus on understanding how AI selects functions automatically

### 👨‍💻 **Intermediate** (Familiar with browser automation)
1. 🔬 Run the complete Jupyter notebook with your own research queries
2. 🛠️ Experiment with modifying function descriptions
3. 🎯 Try customizing agent instructions for different research styles

### 🚀 **Advanced** (Ready for production)
1. 🏗️ Implement additional browser functions (form filling, authentication)
2. 📊 Add structured data extraction capabilities
3. 🔄 Build multi-agent workflows for complex research tasks

---

## 🔑 Key Concepts Covered

### **AI Function Calling Architecture**
- How AI models automatically select and execute functions
- Function description design for optimal AI decision-making
- Sequential function orchestration and error handling

### **Browser Plugin Development** 
- Creating Semantic Kernel plugins with Playwright
- Asynchronous browser operation patterns
- DOM traversal and content extraction strategies

### **Agent Design Patterns**
- Conversational AI that maintains research context
- Agent instruction design for consistent behavior
- Thread management for multi-turn conversations

### **Production Considerations**
- Resource management and browser cleanup
- Error handling and recovery strategies
- Performance optimization for browser operations

---

## 📊 Performance Characteristics

From the notebook demonstrations:
- **Agent Response Time**: 10-30 seconds for complete research tasks
- **Browser Launch**: ~2-3 seconds for initial startup
- **Search Operations**: ~1-2 seconds per Google search
- **Content Extraction**: ~2-5 seconds per page depending on content size
- **AI Model**: GPT-4o-mini with function calling capabilities

---

## 🤝 Learning Support

### 💬 Discussion Topics
- Function calling optimization strategies
- Custom browser automation patterns  
- Multi-agent research workflows
- Integration with other AI services

### 🐛 Common Issues & Solutions
- **Browser launch failures**: Ensure Playwright binaries are installed
- **Element not found errors**: Understanding CSS selector strategies
- **Function calling loops**: Proper error handling in plugin functions
- **Resource cleanup**: Managing browser processes in Jupyter

---

## 🔗 Related Resources

- [Microsoft Semantic Kernel Documentation](https://docs.microsoft.com/en-us/semantic-kernel/)
- [Playwright Documentation](https://playwright.dev/dotnet/)
- [OpenAI Function Calling Guide](https://platform.openai.com/docs/guides/function-calling)
- [.NET Interactive Notebooks](https://github.com/dotnet/interactive)

---

## 🎯 Use Cases

### **Research Automation**
- Academic research with source verification
- Market research and competitive analysis
- News monitoring and trend analysis
- Technical documentation gathering

### **Content Discovery**
- Product research and price comparison
- Event information aggregation
- Contact information extraction
- Social media content analysis

### **Quality Assurance**
- Website functionality testing
- Content validation across multiple sources
- Link checking and verification
- Accessibility testing automation

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

### 🌟 Ready to build intelligent web automation?

**[🎧 Start with Audio](./Assets/sk.mp3)** | **[🔬 Try the Notebook](./SemanticKernel_Agents_Playwright.ipynb)**

*Master AI-powered browser automation with the most comprehensive Playwright agent tutorial available*

</div>
