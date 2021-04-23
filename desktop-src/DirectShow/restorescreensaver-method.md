---
description: Метод Двдадм. Ресторескринсавер восстанавливает системные параметры экранной заставки.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Метод Ресторескринсавер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673004"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="7e02d-103">Метод Ресторескринсавер</span><span class="sxs-lookup"><span data-stu-id="7e02d-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="7e02d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7e02d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7e02d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="7e02d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7e02d-106">`DVDAdm.RestoreScreenSaver`Метод восстанавливает параметры экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="7e02d-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="7e02d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e02d-107">Return Value</span></span>

<span data-ttu-id="7e02d-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7e02d-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e02d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e02d-109">Remarks</span></span>

<span data-ttu-id="7e02d-110">Как правило, приложение DVD отключает экранную заставку системы при запуске, присвоив свойству [**дисаблескринсавер**](disablescreensaver-property.md) значение true, а затем повторно включите экранную заставку при закрытии приложения DVD с помощью вызова `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="7e02d-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="7e02d-111">Если приложение не использует параметры экранной заставки, не нужно вызывать этот метод или задавать свойство **дисаблескринсавер** .</span><span class="sxs-lookup"><span data-stu-id="7e02d-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e02d-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e02d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e02d-113">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="7e02d-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



