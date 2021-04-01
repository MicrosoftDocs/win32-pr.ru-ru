---
title: IDL-файлы
description: IDL-файлы
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891132"
---
# <a name="idl-files"></a><span data-ttu-id="9089e-103">IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="9089e-103">IDL Files</span></span>

<span data-ttu-id="9089e-104">COM использует язык MIDL (MIDL) для описания COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="9089e-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="9089e-105">MIDL является расширением IDL для распределенных вычислительных сред, определенных открытым программным обеспечением, разработанным для определения интерфейсов удаленных вызовов процедур в традиционных клиентских и серверных приложениях.</span><span class="sxs-lookup"><span data-stu-id="9089e-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="9089e-106">MIDL включает большую часть атрибутов и инструкций языка определения объектов (ODL), изначально используемый для создания библиотек типов для OLE-автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9089e-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="9089e-107">В C++ и Java разработчик, создающий объект COM, создает IDL-файл, который компилятор MIDL обрабатывает для создания библиотеки типов, а также для файлов заголовков и прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="9089e-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="9089e-108">*Библиотека типов* — это двоичный файл, ОПИСЫВАЮЩИЙ COM-объект или COM-интерфейсы или оба.</span><span class="sxs-lookup"><span data-stu-id="9089e-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="9089e-109">Библиотека типов — это скомпилированная версия IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="9089e-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="9089e-110">Однако библиотеки типов поддерживают только семантику ODL.</span><span class="sxs-lookup"><span data-stu-id="9089e-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="9089e-111">В частности, они не могут представлять всю информацию из IDL-файла, относящегося к атрибутам IDL \[ [**\_ , например size**](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="9089e-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="9089e-112">Необходимо создать и использовать прокси-файлы для файлов IDL, затронутых потерей информации в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="9089e-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="9089e-113">В Visual Basic разработчик, создающий объект COM, не создает IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="9089e-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="9089e-114">Вместо этого Visual Basic собирает сведения с помощью свойств класса и проекта и непосредственно создает библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="9089e-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 