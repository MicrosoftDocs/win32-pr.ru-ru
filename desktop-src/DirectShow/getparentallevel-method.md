---
description: Метод Двдадм. Жетпаренталлевел получает родительский уровень, который был сохранен в реестре в последний раз.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Метод Жетпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416440"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="71dc6-103">Метод Жетпаренталлевел</span><span class="sxs-lookup"><span data-stu-id="71dc6-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="71dc6-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="71dc6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="71dc6-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="71dc6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="71dc6-106">`DVDAdm.GetParentalLevel`Метод получает родительский уровень, который был сохранен в реестре последним.</span><span class="sxs-lookup"><span data-stu-id="71dc6-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="71dc6-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71dc6-107">Return Value</span></span>

<span data-ttu-id="71dc6-108">Возвращает целое число от 1 до 8, указывающее на родительский уровень по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71dc6-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="71dc6-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71dc6-109">Remarks</span></span>

<span data-ttu-id="71dc6-110">Родительский уровень, получаемый этим методом, не обязательно является тем же уровнем, который в настоящее время хранится в элементе управления Мсвебдвд; чтобы получить уровень, хранящийся в данный момент в элементе управления, вызовите метод [**жетплайерпаренталлевел**](getplayerparentallevel-method.md) .</span><span class="sxs-lookup"><span data-stu-id="71dc6-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="71dc6-111">Значение-1 указывает на то, что функция родительского управления отключена.</span><span class="sxs-lookup"><span data-stu-id="71dc6-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="71dc6-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71dc6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dc6-113">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="71dc6-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



