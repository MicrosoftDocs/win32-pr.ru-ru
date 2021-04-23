---
description: Свойство Двдадм предоставляет доступ к объекту Мсдвдадм, содержащему методы и свойства для сохранения сведений о приложении и пользователе.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Двдадм, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140042"
---
# <a name="dvdadm-property"></a><span data-ttu-id="73b06-103">Двдадм, свойство</span><span class="sxs-lookup"><span data-stu-id="73b06-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="73b06-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73b06-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="73b06-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="73b06-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="73b06-106">`DVDAdm`Свойство предоставляет доступ к объекту [мсдвдадм](msdvdadm-object.md) , содержащему методы и свойства для сохранения сведений о приложении и пользователе.</span><span class="sxs-lookup"><span data-stu-id="73b06-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="73b06-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73b06-107">Remarks</span></span>

<span data-ttu-id="73b06-108">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73b06-108">This property is read-only with no default value.</span></span> <span data-ttu-id="73b06-109">Нет необходимости создавать отдельную ссылку на объект **мсдвдадм** .</span><span class="sxs-lookup"><span data-stu-id="73b06-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="73b06-110">Чтобы получить доступ к методам и свойствам объекта, используйте `DVDAdm` свойство, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="73b06-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="73b06-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="73b06-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



