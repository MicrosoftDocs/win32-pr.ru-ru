---
description: Доступ к неименованному значению реестра
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Доступ к неименованному значению реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703007"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="1377e-103">Доступ к неименованному значению реестра</span><span class="sxs-lookup"><span data-stu-id="1377e-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="1377e-104">По умолчанию или безымянное значение раздела реестра отображается как (по умолчанию) или <No Name> в редакторе реестра Regedit.</span><span class="sxs-lookup"><span data-stu-id="1377e-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="1377e-105">Для доступа к неименованному разделу реестра можно использовать поставщик системного реестра.</span><span class="sxs-lookup"><span data-stu-id="1377e-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="1377e-106">Аналогично, можно также использовать поставщик системного реестра для доступа к описаниям точечных рисунков, которые определены как безымянные значения.</span><span class="sxs-lookup"><span data-stu-id="1377e-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="1377e-107">В следующей процедуре описывается, как получить неименованное значение реестра.</span><span class="sxs-lookup"><span data-stu-id="1377e-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="1377e-108">**Получение неименованного значения реестра**</span><span class="sxs-lookup"><span data-stu-id="1377e-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="1377e-109">Определите свойство и задайте в качестве квалификатора **пропертиконтекст** этого свойства пустую строку.</span><span class="sxs-lookup"><span data-stu-id="1377e-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="1377e-110">В следующем примере кода показано, как класс определяет свойства для хранения значений ключа, заданного квалификатором **классконтекст** .</span><span class="sxs-lookup"><span data-stu-id="1377e-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="1377e-111">Значение по умолчанию хранится в свойстве **по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="1377e-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="1377e-112">Ключ транспортов не использует безымянное значение, поэтому компиляция этого MOF-файла не создает никакого значения для свойства **по умолчанию** , если только средство редактирования реестра не используется для изменения безымянного значения.</span><span class="sxs-lookup"><span data-stu-id="1377e-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="1377e-113">Для файла точечного рисунка определите свойство и задайте **пропертиконтекст** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="1377e-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="1377e-114">В следующем примере кода показано, как определить свойство.</span><span class="sxs-lookup"><span data-stu-id="1377e-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



