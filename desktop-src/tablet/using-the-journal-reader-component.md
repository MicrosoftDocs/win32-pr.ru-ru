---
description: Компонент чтения заметок журнала Microsoft Windows предоставляет программный доступ на чтение файлов в формате журнала.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Использование компонента чтения журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991084"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="1eda9-103">Использование компонента чтения журнала</span><span class="sxs-lookup"><span data-stu-id="1eda9-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="1eda9-104">Компонент чтения заметок журнала Microsoft Windows предоставляет программный доступ на чтение файлов в формате журнала.</span><span class="sxs-lookup"><span data-stu-id="1eda9-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="1eda9-105">Обзор компонентов</span><span class="sxs-lookup"><span data-stu-id="1eda9-105">Component Overview</span></span>

<span data-ttu-id="1eda9-106">Файлы журнала имеют расширение. jnt.</span><span class="sxs-lookup"><span data-stu-id="1eda9-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="1eda9-107">Этот простой компонент принимает поток, содержащий JNT-файл, и возвращает поток, содержащий содержимое файла в формате XML.</span><span class="sxs-lookup"><span data-stu-id="1eda9-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="1eda9-108">XML-код, возвращаемый компонентом, соответствует схеме чтения заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="1eda9-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="1eda9-109">Эта схема описана в [справочнике по схеме чтения журнала](journal-reader-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1eda9-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="1eda9-110">Компонент не предоставляет возможность записи файлов. jnt.</span><span class="sxs-lookup"><span data-stu-id="1eda9-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="1eda9-111">Компонент доступен в неуправляемых и управляемых версиях.</span><span class="sxs-lookup"><span data-stu-id="1eda9-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="1eda9-112">Неуправляемый компонент доступен в библиотеке динамической компоновки (DLL) journal.dll.</span><span class="sxs-lookup"><span data-stu-id="1eda9-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="1eda9-113">Управляемая версия находится либо в Microsoft.Ink.Journal.dll сборке (для повторного распространения на Windows XP Tablet PC Edition, либо в Windows Vista), либо Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="1eda9-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1eda9-114">Начиная с Windows 10 версии 1607, journal.dll не входит в состав операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="1eda9-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="1eda9-115">Эта библиотека должна считаться устаревшей или устаревшей и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="1eda9-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="1eda9-116">Изменения в сборке заметки</span><span class="sxs-lookup"><span data-stu-id="1eda9-116">Assembly Changes of Note</span></span>

<span data-ttu-id="1eda9-117">Важно помнить о некоторых изменениях в сборке, содержащей компонент чтения примечаний журнала, который был выпущен в сочетании с версией 1,7 набора разработчиков планшетов и версией, поставляемой в составе операционной системы Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1eda9-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="1eda9-118">Версия 1,7 компонента чтения, которую можно распространить на Windows XP или Windows Vista, содержится в сборке с именем Microsoft.Ink.Journal.dll.</span><span class="sxs-lookup"><span data-stu-id="1eda9-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="1eda9-119">Компонент Reader поставляется в составе Windows Vista, но интегрирован в основную Microsoft.Ink.dll сборку.</span><span class="sxs-lookup"><span data-stu-id="1eda9-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="1eda9-120">Это означает, что приложения, использующие сборку 1,7, должны повторно распространять эту сборку с помощью программы установки.</span><span class="sxs-lookup"><span data-stu-id="1eda9-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="1eda9-121">Использование компонента</span><span class="sxs-lookup"><span data-stu-id="1eda9-121">Using the Component</span></span>

<span data-ttu-id="1eda9-122">Компонент чтения заметок журнала полезен для извлечения данных рукописного ввода и других сведений о файле из файла журнала.</span><span class="sxs-lookup"><span data-stu-id="1eda9-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="1eda9-123">COM</span><span class="sxs-lookup"><span data-stu-id="1eda9-123">COM</span></span>

<span data-ttu-id="1eda9-124">Компонент COM для чтения заметки журнала находится в файле Journal.dll, который устанавливается и регистрируется при скачивании и запуске файла установки средства чтения заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="1eda9-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="1eda9-125">Компонент COM не поддерживает интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1eda9-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="1eda9-126">управляемость.</span><span class="sxs-lookup"><span data-stu-id="1eda9-126">Managed</span></span>

<span data-ttu-id="1eda9-127">Управляемый компонент чтения заметки журнала находится в сборке Microsoft.Ink.JournalReader.dll.</span><span class="sxs-lookup"><span data-stu-id="1eda9-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="1eda9-128">Эта сборка устанавливается и регистрируется в глобальном кэше сборок при запуске файла установки средства чтения заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="1eda9-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="1eda9-129">Добавьте ссылку на сборку, чтобы использовать ее в управляемом проекте.</span><span class="sxs-lookup"><span data-stu-id="1eda9-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eda9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1eda9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eda9-131">**Интерфейс Ижаурналреадер**</span><span class="sxs-lookup"><span data-stu-id="1eda9-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="1eda9-132">Справочник по схеме чтения журнала</span><span class="sxs-lookup"><span data-stu-id="1eda9-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
