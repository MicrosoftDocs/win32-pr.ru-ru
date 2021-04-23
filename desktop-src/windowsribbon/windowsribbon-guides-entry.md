---
title: Руководства для разработчиков платформы Windows Ribbon
description: Разделы, содержащиеся в этом разделе, описывают конкретные аспекты платформы Windows Ribbon.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Лента Windows, платформа
- Лента, платформа
- Лента Windows, руководства для разработчиков
- Лента, руководства для разработчиков
- направляющие для разработчиков для ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134390"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="3e6ad-108">Руководства для разработчиков платформы Windows Ribbon</span><span class="sxs-lookup"><span data-stu-id="3e6ad-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="3e6ad-109">Разделы, содержащиеся в этом разделе, описывают конкретные аспекты платформы Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="3e6ad-110">Основы</span><span class="sxs-lookup"><span data-stu-id="3e6ad-110">Basics</span></span>

[<span data-ttu-id="3e6ad-111">Создание приложения для ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="3e6ad-112">Чтобы платформа Windows Ribbon использовала файл разметки ленты, файл разметки должен быть скомпилирован в файл ресурсов в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="3e6ad-113">Для этой цели в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows входит выделенный компилятор разметки ленты (УИКК) (7,0 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="3e6ad-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="3e6ad-114">Помимо компиляции двоичной версии разметки ленты, УИКК создает файл заголовка определения идентификатора (. h), который предоставляет все элементы разметки для хост-приложения ленты и файл ресурсов (. RC), который используется для связывания ресурсов Image и String с ведущим приложением во время сборки.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="3e6ad-115">Переход на платформу Windows Ribbon</span><span class="sxs-lookup"><span data-stu-id="3e6ad-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="3e6ad-116">Приложение, основанное на традиционных меню, панелях инструментов и диалоговых окнах, может быть перенесено в многофункциональный, динамический и контекстный пользовательский интерфейс, основанный на контексте командной системы платформы Ribbon.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="3e6ad-117">Это простой и эффективный способ модернизировать и ревитализе приложение, одновременно улучшая доступность, удобство использования и возможность обнаружения его функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="3e6ad-118">Основные сведения о командах и элементах управления</span><span class="sxs-lookup"><span data-stu-id="3e6ad-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="3e6ad-119">Разделение логики из представления является философией проектирования, инспирес систему представления команд платформы Ribbon — систему, основанную на шаблоне разработки, где функциональность и поведение реализуются независимо от элементов управления, предоставляющих эти функции.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="3e6ad-120">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="3e6ad-120">User Interface</span></span>

[<span data-ttu-id="3e6ad-121">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="3e6ad-122">Как многофункциональная система представления команд, платформа Ribbon разработана для широкого создания графических ресурсов на протяжении всего пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="3e6ad-123">Все ресурсы изображений объявляются в [разметке ленты](windowsribbon-schema.md) или запрашиваются из хост-приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="3e6ad-124">Для Windows 8 и более поздних версий платформа Ribbon поддерживает следующие форматы графики: 32-битовые растровые файлы ARGB (BMP) и PNG-файлы с прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="3e6ad-125">Для Windows 7 и более ранних версий ресурсы образа должны соответствовать стандартному графическому формату BMP, используемому в Windows.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="3e6ad-126">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="3e6ad-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="3e6ad-127">Элементы управления, размещенные на панели команд ленты, подчиняются правилам макета, которые применяются платформой Ribbon и основаны на сочетаниях поведения по умолчанию и шаблонов макета (определяемых платформой и настраиваемых), как объявлено в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="3e6ad-128">Эти правила определяют поведение адаптивного макета для платформы Ribbon, влияющее на то, как элементы управления на панели команд адаптируются к различным размерам ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="3e6ad-129">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="3e6ad-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="3e6ad-130">Платформа Ribbon предоставляет разработчикам надежную и согласованную модель управления динамическим содержимым в различных элементах управления, основанных на коллекциях.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="3e6ad-131">Адаптируя и перестраивая пользовательский интерфейс Ribbon, эти динамические элементы управления позволяют платформе реагировать на взаимодействие с пользователем как в ведущем приложении, так и на ленте, а также обеспечивают гибкость при обработке различных сред выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="3e6ad-132">Отображение контекстных вкладок</span><span class="sxs-lookup"><span data-stu-id="3e6ad-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="3e6ad-133">В приложении платформы Ribbon контекстная вкладка — это скрытый элемент управления ["Вкладка](windowsribbon-controls-tab.md) ", который отображается в строке вкладки при выборе или выделении объекта в рабочей области приложения, например изображения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="3e6ad-134">Перенастройка ленты с помощью режимов приложения</span><span class="sxs-lookup"><span data-stu-id="3e6ad-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="3e6ad-135">Платформа Ribbon поддерживает динамическую перенастройку и предоставление основных элементов пользовательского интерфейса ленты во время выполнения на основе состояния приложения (также называемого контекстом).</span><span class="sxs-lookup"><span data-stu-id="3e6ad-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="3e6ad-136">Объявления и связанные с определенными элементами в разметке, различные состояния, поддерживаемые приложением, называются режимами приложения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="3e6ad-137">Настройка цветов ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="3e6ad-138">Платформа Ribbon предоставляет набор свойств цвета, позволяющих приложению настраивать внешний вид различных элементов ПОЛЬЗОВАТЕЛЬСКОГО интерфейса ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="3e6ad-139">Отображение ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="3e6ad-140">Платформа Ribbon предоставляет набор свойств, позволяющих приложению указать способ отображения ПОЛЬЗОВАТЕЛЬСКОГО интерфейса ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="3e6ad-141">Управление</span><span class="sxs-lookup"><span data-stu-id="3e6ad-141">Management</span></span>

[<span data-ttu-id="3e6ad-142">Сохранение состояния ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="3e6ad-143">Платформа Windows рибон Framework (лента) предоставляет возможность сохранения состояния различных параметров и настроек пользователей во всех сеансах приложения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="3e6ad-144">Прослушивание событий ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="3e6ad-145">Платформа Ribbon использует инфраструктуру [трассировки событий для Windows (ETW)](../etw/event-tracing-portal.md) , позволяющую разработчикам узнать, как пользователи взаимодействуют с лентой приложения.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="3e6ad-146">Компилятор разметки</span><span class="sxs-lookup"><span data-stu-id="3e6ad-146">Markup Compiler</span></span>

[<span data-ttu-id="3e6ad-147">Компиляция разметки ленты</span><span class="sxs-lookup"><span data-stu-id="3e6ad-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="3e6ad-148">Чтобы платформа Ribbon использовала файл [разметки ленты](windowsribbon-schema.md) , файл разметки должен быть скомпилирован в файл ресурсов в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="3e6ad-149">Для этой цели в составе пакета средств разработки программного обеспечения (SDK) для Microsoft Windows входит выделенный компилятор разметки, компилятор команд пользовательского интерфейса (УИКК) (7,0 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="3e6ad-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="3e6ad-150">Помимо компиляции двоичной версии разметки, УИКК создает файл заголовка определения идентификатора (. h), который предоставляет все элементы разметки для хост-приложения ленты и файл ресурсов (. RC), который используется для связывания ресурсов Image и String с ведущим приложением во время сборки.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="3e6ad-151">Основные сведения о сообщениях компилятора разметки</span><span class="sxs-lookup"><span data-stu-id="3e6ad-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="3e6ad-152">Компилятор разметки платформы Windows Ribbon Framework (лента), компилятор команд пользовательского интерфейса (UICC.exe) проверяет разметку ленты на соответствие схеме ленты и дополнительном наборе правил, определенных платформой Ribbon.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 