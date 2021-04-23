---
title: Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)
description: Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134135"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="b47b8-103">Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)</span><span class="sxs-lookup"><span data-stu-id="b47b8-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="b47b8-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="b47b8-104">Platforms</span></span>

<dl> <span data-ttu-id="b47b8-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b47b8-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="b47b8-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b47b8-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="b47b8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b47b8-107">Description</span></span>

<span data-ttu-id="b47b8-108">Следующие API диспетчера методов ввода не поддерживаются упрощенными редакторами IME в Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="b47b8-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="b47b8-109">Интерфейс Ифекоммон</span><span class="sxs-lookup"><span data-stu-id="b47b8-109">IFECommon interface</span></span>
-   <span data-ttu-id="b47b8-110">Интерфейс Ифедиктионари</span><span class="sxs-lookup"><span data-stu-id="b47b8-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="b47b8-111">Интерфейс Ифелангуаже</span><span class="sxs-lookup"><span data-stu-id="b47b8-111">IFELanguage interface</span></span>
-   <span data-ttu-id="b47b8-112">Интерфейс Иимепад</span><span class="sxs-lookup"><span data-stu-id="b47b8-112">IImePad interface</span></span>
-   <span data-ttu-id="b47b8-113">Интерфейс Иимепадапплет</span><span class="sxs-lookup"><span data-stu-id="b47b8-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="b47b8-114">Интерфейс ИимеспеЦифяпплетс</span><span class="sxs-lookup"><span data-stu-id="b47b8-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="b47b8-115">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="b47b8-115">Manifestations</span></span>

<span data-ttu-id="b47b8-116">Функции, использующие эти API, не работают с упрощенным IME.</span><span class="sxs-lookup"><span data-stu-id="b47b8-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="b47b8-117">Решение</span><span class="sxs-lookup"><span data-stu-id="b47b8-117">Solution</span></span>

<span data-ttu-id="b47b8-118">Приложения должны быть спроектированы таким образом, чтобы пользователи могли выполнять нужную задачу без использования указанного API.</span><span class="sxs-lookup"><span data-stu-id="b47b8-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="b47b8-119">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="b47b8-119">Resources</span></span>

-   [<span data-ttu-id="b47b8-120">Интерфейсы диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="b47b8-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="b47b8-121">ифекоммон</span><span class="sxs-lookup"><span data-stu-id="b47b8-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="b47b8-122">Интерфейс Ифекоммон</span><span class="sxs-lookup"><span data-stu-id="b47b8-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="b47b8-123">Интерфейс Ифедиктионари</span><span class="sxs-lookup"><span data-stu-id="b47b8-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="b47b8-124">ифелангуаже</span><span class="sxs-lookup"><span data-stu-id="b47b8-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="b47b8-125">иимепад</span><span class="sxs-lookup"><span data-stu-id="b47b8-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="b47b8-126">иимепадапплет</span><span class="sxs-lookup"><span data-stu-id="b47b8-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="b47b8-127">иимеплугиндиктдиктионарилист</span><span class="sxs-lookup"><span data-stu-id="b47b8-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="b47b8-128">иимеспеЦифяпплетс</span><span class="sxs-lookup"><span data-stu-id="b47b8-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 