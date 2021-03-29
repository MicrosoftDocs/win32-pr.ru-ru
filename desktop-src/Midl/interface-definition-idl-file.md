---
title: Файл определения интерфейса (IDL)
description: По соглашению файл, содержащий определения интерфейсов и библиотек типов, называется IDL-файлом и имеет расширение IDL.
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- интерфейс MIDL, IDL-файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950daa2c1841f6e4b3f015f14e373804fcd34b80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790224"
---
# <a name="interface-definition-idl-file"></a><span data-ttu-id="e52fe-104">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e52fe-104">Interface Definition (IDL) File</span></span>

<span data-ttu-id="e52fe-105">По соглашению файл, содержащий определения интерфейсов и библиотек типов, называется IDL-файлом и имеет расширение IDL.</span><span class="sxs-lookup"><span data-stu-id="e52fe-105">By convention, the file that contains interface and type library definitions is called an IDL file, and has an .idl file name extension.</span></span> <span data-ttu-id="e52fe-106">На практике компилятор MIDL будет анализировать файл определения интерфейса независимо от его расширения.</span><span class="sxs-lookup"><span data-stu-id="e52fe-106">In reality, the MIDL compiler will parse an interface definition file regardless of its extension.</span></span> <span data-ttu-id="e52fe-107">Интерфейс определяется с помощью ключевого слова [**Interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="e52fe-107">An interface is identified by the keyword [**interface**](interface.md).</span></span>

<span data-ttu-id="e52fe-108">Каждый интерфейс состоит из заголовка и тела.</span><span class="sxs-lookup"><span data-stu-id="e52fe-108">Each interface consists of a header and a body.</span></span> <span data-ttu-id="e52fe-109">Заголовок интерфейса содержит атрибуты, которые применяются ко всему интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="e52fe-109">The interface header contains attributes that apply to the entire interface.</span></span> <span data-ttu-id="e52fe-110">Тело интерфейса содержит оставшиеся определения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e52fe-110">The body of the interface contains the remaining interface definitions.</span></span> <span data-ttu-id="e52fe-111">Обзор интерфейсов и IDL-файлов см. [в разделе IDL-файл](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span><span class="sxs-lookup"><span data-stu-id="e52fe-111">For an overview of interfaces and IDL files, see [The Interface Definition Language (IDL) File](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span></span> <span data-ttu-id="e52fe-112">Общие сведения об атрибутах, которые можно использовать в заголовке интерфейса, см. в разделе [атрибуты IDL](idl-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e52fe-112">For a summary of attributes that can be used in an interface header, see [IDL Attributes](idl-attributes.md).</span></span>

 

 