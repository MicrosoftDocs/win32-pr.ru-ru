---
description: Средство Мфтраце может читать XML-файл конфигурации, указывающий одного или нескольких поставщиков трассировки.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Файл конфигурации Мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650664"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="13f2b-103">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="13f2b-103">MFTrace Configuration File</span></span>

<span data-ttu-id="13f2b-104">Средство [мфтраце](mftrace.md) может читать XML-файл конфигурации, указывающий одного или нескольких поставщиков трассировки.</span><span class="sxs-lookup"><span data-stu-id="13f2b-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="13f2b-105">Элемент [**providers**](providers.md) является корневым элементом в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="13f2b-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13f2b-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="13f2b-106">In this section</span></span>

-   [<span data-ttu-id="13f2b-107">**This**</span><span class="sxs-lookup"><span data-stu-id="13f2b-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="13f2b-108">**мфдетаурс**</span><span class="sxs-lookup"><span data-stu-id="13f2b-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="13f2b-109">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="13f2b-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="13f2b-110">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="13f2b-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="13f2b-111">Пример</span><span class="sxs-lookup"><span data-stu-id="13f2b-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="13f2b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="13f2b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f2b-113">мфтраце</span><span class="sxs-lookup"><span data-stu-id="13f2b-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



