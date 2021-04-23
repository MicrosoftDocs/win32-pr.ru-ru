---
title: Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается
description: Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791922"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="e06e9-103">Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e06e9-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="e06e9-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="e06e9-104">Platforms</span></span>

<dl> <span data-ttu-id="e06e9-105">Клиенты — Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="e06e9-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="e06e9-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e06e9-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="e06e9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e06e9-107">Description</span></span>

<span data-ttu-id="e06e9-108">Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложения Магазина Windows не поддерживается и может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="e06e9-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="e06e9-109">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="e06e9-109">Manifestations</span></span>

<span data-ttu-id="e06e9-110">При запуске приложения в режиме IME задаются следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="e06e9-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="e06e9-111">Панель программного ввода</span><span class="sxs-lookup"><span data-stu-id="e06e9-111">Software input panel</span></span> | <span data-ttu-id="e06e9-112">Аппаратная клавиатура</span><span class="sxs-lookup"><span data-stu-id="e06e9-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="e06e9-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="e06e9-113">KOR, JPN</span></span> | <span data-ttu-id="e06e9-114">С</span><span class="sxs-lookup"><span data-stu-id="e06e9-114">On</span></span>                   | <span data-ttu-id="e06e9-115">Выкл.</span><span class="sxs-lookup"><span data-stu-id="e06e9-115">Off</span></span>               |
| <span data-ttu-id="e06e9-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="e06e9-116">CHS, CHT</span></span> | <span data-ttu-id="e06e9-117">Включено</span><span class="sxs-lookup"><span data-stu-id="e06e9-117">On</span></span>                   | <span data-ttu-id="e06e9-118">Включено</span><span class="sxs-lookup"><span data-stu-id="e06e9-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="e06e9-119">Решение</span><span class="sxs-lookup"><span data-stu-id="e06e9-119">Solution</span></span>

<span data-ttu-id="e06e9-120">Разработчики могут управлять режимом IME по умолчанию, указывая значение области ввода для поля.</span><span class="sxs-lookup"><span data-stu-id="e06e9-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="e06e9-121">Режим IME для заданной области ввода определяется каждым IME.</span><span class="sxs-lookup"><span data-stu-id="e06e9-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="e06e9-122">Разработчики не могут указать режим IME.</span><span class="sxs-lookup"><span data-stu-id="e06e9-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="e06e9-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="e06e9-123">Resources</span></span>

-   [<span data-ttu-id="e06e9-124">Перечисление Инпутскопе</span><span class="sxs-lookup"><span data-stu-id="e06e9-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="e06e9-125">иммсетконверсионстатус</span><span class="sxs-lookup"><span data-stu-id="e06e9-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="e06e9-126">[иммжетконверсионстатус](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e06e9-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 