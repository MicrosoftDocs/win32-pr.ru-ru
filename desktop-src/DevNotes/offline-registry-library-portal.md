---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Библиотека автономных разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662071"
---
# <a name="offline-registry-library"></a><span data-ttu-id="04f29-103">Библиотека автономных разделов реестра</span><span class="sxs-lookup"><span data-stu-id="04f29-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="04f29-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="04f29-104">Purpose</span></span>

<span data-ttu-id="04f29-105">Библиотека автономных разделов реестра (Offreg.dll) используется для изменения куста реестра за пределами активного системного реестра.</span><span class="sxs-lookup"><span data-stu-id="04f29-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="04f29-106">Эта библиотека предназначена для сценариев обновления реестра, таких как обслуживание образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="04f29-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="04f29-107">Библиотека поддерживает форматы кустов реестра, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04f29-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04f29-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="04f29-108">Developer audience</span></span>

<span data-ttu-id="04f29-109">Эта технология предназначена для изготовителей оборудования (OEM), антивирусных и антивредоносных программ, а также для других разработчиков приложений, которые должны иметь возможность анализировать файлы Hive реестра, не загружая их в активный реестр.</span><span class="sxs-lookup"><span data-stu-id="04f29-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04f29-110">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="04f29-110">Run-time requirements</span></span>

<span data-ttu-id="04f29-111">Автономная библиотека реестра предоставляется в виде библиотеки динамической компоновки (DLL), распространяемой в виде двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="04f29-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="04f29-112">Эта библиотека работает на следующих версиях Windows:</span><span class="sxs-lookup"><span data-stu-id="04f29-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="04f29-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04f29-113">Windows Server 2016</span></span>  
<span data-ttu-id="04f29-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04f29-114">Windows 10</span></span>  
<span data-ttu-id="04f29-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="04f29-115">Windows 8.1</span></span>  
<span data-ttu-id="04f29-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04f29-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="04f29-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04f29-117">Windows 8</span></span>  
<span data-ttu-id="04f29-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04f29-118">Windows Server 2012</span></span>  
<span data-ttu-id="04f29-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04f29-119">Windows 7</span></span>  
<span data-ttu-id="04f29-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04f29-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="04f29-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04f29-121">Windows Server 2008</span></span>  
<span data-ttu-id="04f29-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04f29-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="04f29-123">Приложения должны ссылаться на Offreg.dll с помощью динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="04f29-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="04f29-124">Offreg.dll предоставляется в комплекте драйверов Windows (WDK) для Windows 10 и более ранних версий операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="04f29-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="04f29-125">Сведения о получении WDK см. в статье [как получить WDK и Влк](/windows-hardware/drivers/download-the-wdk) или посетить веб-сайт [подписок MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="04f29-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04f29-126">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="04f29-126">In this section</span></span>

-   [<span data-ttu-id="04f29-127">**Сведения о библиотеке автономных разделов реестра**</span><span class="sxs-lookup"><span data-stu-id="04f29-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="04f29-128">**Функции библиотеки автономного реестра**</span><span class="sxs-lookup"><span data-stu-id="04f29-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
