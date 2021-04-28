---
description: Библиотека автономных разделов реестра
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Библиотека автономных разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089252"
---
# <a name="offline-registry-library"></a><span data-ttu-id="c6ed5-103">Библиотека автономных разделов реестра</span><span class="sxs-lookup"><span data-stu-id="c6ed5-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="c6ed5-104">Цель</span><span class="sxs-lookup"><span data-stu-id="c6ed5-104">Purpose</span></span>

<span data-ttu-id="c6ed5-105">Библиотека автономных разделов реестра (Offreg.dll) используется для изменения куста реестра за пределами активного системного реестра.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="c6ed5-106">Эта библиотека предназначена для сценариев обновления реестра, таких как обслуживание образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="c6ed5-107">Библиотека поддерживает форматы кустов реестра, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c6ed5-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c6ed5-108">Developer audience</span></span>

<span data-ttu-id="c6ed5-109">Эта технология предназначена для изготовителей оборудования (OEM), антивирусных и антивредоносных программ, а также для других разработчиков приложений, которые должны иметь возможность анализировать файлы Hive реестра, не загружая их в активный реестр.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c6ed5-110">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c6ed5-110">Run-time requirements</span></span>

<span data-ttu-id="c6ed5-111">Автономная библиотека реестра предоставляется в виде библиотеки динамической компоновки (DLL), распространяемой в виде двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="c6ed5-112">Эта библиотека работает на следующих версиях Windows:</span><span class="sxs-lookup"><span data-stu-id="c6ed5-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="c6ed5-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c6ed5-113">Windows Server 2016</span></span>  
<span data-ttu-id="c6ed5-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c6ed5-114">Windows 10</span></span>  
<span data-ttu-id="c6ed5-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c6ed5-115">Windows 8.1</span></span>  
<span data-ttu-id="c6ed5-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6ed5-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="c6ed5-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6ed5-117">Windows 8</span></span>  
<span data-ttu-id="c6ed5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6ed5-118">Windows Server 2012</span></span>  
<span data-ttu-id="c6ed5-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6ed5-119">Windows 7</span></span>  
<span data-ttu-id="c6ed5-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6ed5-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="c6ed5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6ed5-121">Windows Server 2008</span></span>  
<span data-ttu-id="c6ed5-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6ed5-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="c6ed5-123">Приложения должны ссылаться на Offreg.dll с помощью динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="c6ed5-124">Offreg.dll предоставляется в комплекте драйверов Windows (WDK) для Windows 10 и более ранних версий операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c6ed5-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="c6ed5-125">Сведения о получении WDK см. в статье [как получить WDK и Влк](/windows-hardware/drivers/download-the-wdk) или посетить веб-сайт [подписок MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c6ed5-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6ed5-126">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c6ed5-126">In this section</span></span>

-   [<span data-ttu-id="c6ed5-127">**Сведения о библиотеке автономных разделов реестра**</span><span class="sxs-lookup"><span data-stu-id="c6ed5-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="c6ed5-128">**Функции библиотеки автономного реестра**</span><span class="sxs-lookup"><span data-stu-id="c6ed5-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
