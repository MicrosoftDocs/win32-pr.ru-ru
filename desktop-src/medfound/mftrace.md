---
description: Мфтраце — это средство для создания журналов трассировки для Media Foundation приложений.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651655"
---
# <a name="mftrace"></a><span data-ttu-id="bbabe-103">мфтраце</span><span class="sxs-lookup"><span data-stu-id="bbabe-103">MFTrace</span></span>

<span data-ttu-id="bbabe-104">Мфтраце — это средство для создания журналов трассировки для Media Foundation приложений.</span><span class="sxs-lookup"><span data-stu-id="bbabe-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bbabe-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="bbabe-105">In this section</span></span>

-   [<span data-ttu-id="bbabe-106">Использование Мфтраце</span><span class="sxs-lookup"><span data-stu-id="bbabe-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="bbabe-107">Ключевые слова Мфтраце</span><span class="sxs-lookup"><span data-stu-id="bbabe-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="bbabe-108">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="bbabe-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="bbabe-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bbabe-109">Requirements</span></span>



| <span data-ttu-id="bbabe-110">Требование</span><span class="sxs-lookup"><span data-stu-id="bbabe-110">Requirement</span></span> | <span data-ttu-id="bbabe-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bbabe-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbabe-112">Минимальная версия пакета SDK</span><span class="sxs-lookup"><span data-stu-id="bbabe-112">Minimum SDK version</span></span>      | <span data-ttu-id="bbabe-113">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="bbabe-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="bbabe-114">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="bbabe-114">Minimum operating system</span></span> | <span data-ttu-id="bbabe-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbabe-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="bbabe-116">Для Мфтраце требуются следующие библиотеки DLL, которые также предоставляются в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="bbabe-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="bbabe-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="bbabe-117">detoured.dll</span></span>
-   <span data-ttu-id="bbabe-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="bbabe-118">mfdetours.dll</span></span>

<span data-ttu-id="bbabe-119">Пакет SDK предоставляет как 32-разрядную, так и 64-разрядную версию Мфтраце.</span><span class="sxs-lookup"><span data-stu-id="bbabe-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="bbabe-120">Мфтраце не поддерживает WOW64; для трассировки 32-разрядного процесса, выполняющегося в 64-разрядной версии Windows, используйте 32-bit Мфтраце.</span><span class="sxs-lookup"><span data-stu-id="bbabe-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="bbabe-121">пакет SDK-root на 32-разрядных системах: \Program Files\Windows Kits\10 SDK-root на 64 разрядной системе: \Program Files (x86) \Windows Kits\10 вы найдете мфтраце по адресу <SDK — root> \bin \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="bbabe-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbabe-122">См. также</span><span class="sxs-lookup"><span data-stu-id="bbabe-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbabe-123">Средства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbabe-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



