---
title: Что видят клиенты
description: В этом разделе перечислены способы, с помощью которых клиент просматривает данные ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- расширения ADSI, что видят клиенты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533494"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="946d6-104">Что видят клиенты?</span><span class="sxs-lookup"><span data-stu-id="946d6-104">What Does a Client See?</span></span>

-   <span data-ttu-id="946d6-105">Клиент видит ADSI и все его объекты расширения как один объект.</span><span class="sxs-lookup"><span data-stu-id="946d6-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="946d6-106">Клиент ADSI видит один интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , который обрабатывает все сдвоенные и отправляемые интерфейсы в объекте, независимо от того, реализуется ли сдвоенный или исправный интерфейс агрегатором в поставщике или расширением.</span><span class="sxs-lookup"><span data-stu-id="946d6-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="946d6-107">Ознакомьтесь с [разрешениями конфликтов имен функций и свойств в службе автоматизации в расширениях](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="946d6-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="946d6-108">ADSI не предоставляет никаких сведений о типе с помощью методов [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) или [**IDispatch:: жеттипеинфокаунт**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) .</span><span class="sxs-lookup"><span data-stu-id="946d6-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="946d6-109">ADSI предоставляет сведения о типах с помощью библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="946d6-109">ADSI provides type information through the type library.</span></span>

 

 