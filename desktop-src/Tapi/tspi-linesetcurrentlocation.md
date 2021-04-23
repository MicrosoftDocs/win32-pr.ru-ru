---
description: Эта \_ функция ЛИНЕСЕТКУРРЕНТЛОКАТИОН тспи устарела. TAPI вызывает эту функцию, когда пользователь (с помощью диалогового окна Свойства набора номера) или приложение (с помощью функции Линесеткуррентлокатион) изменили расположение преобразования адресов.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814361"
---
# <a name="tspi_linesetcurrentlocation"></a><span data-ttu-id="817cb-104">ТСПИ \_ линесеткуррентлокатион</span><span class="sxs-lookup"><span data-stu-id="817cb-104">TSPI\_lineSetCurrentLocation</span></span>

<span data-ttu-id="817cb-105">Эта \_ функция ЛИНЕСЕТКУРРЕНТЛОКАТИОН тспи устарела.</span><span class="sxs-lookup"><span data-stu-id="817cb-105">This TSPI\_lineSetCurrentLocation function is obsolete.</span></span> <span data-ttu-id="817cb-106">TAPI вызывает эту функцию, когда пользователь (с помощью диалогового окна **Свойства набора номера** ) или приложение (с помощью функции [**линесеткуррентлокатион**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) изменили расположение преобразования адресов.</span><span class="sxs-lookup"><span data-stu-id="817cb-106">TAPI called this function when the user (using the **Dialing Properties** dialog box) or an application (using the [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) function) changed the address translation location.</span></span>

<span data-ttu-id="817cb-107">В настоящее время изменение расположения перевода приводит к постановке в строку \_ сообщения девстате с *dwParam1* , для которого задано значение линедевстате \_ транслатечанже.</span><span class="sxs-lookup"><span data-stu-id="817cb-107">Currently, a change in translation location results in a LINE\_DEVSTATE message with *dwParam1* set to LINEDEVSTATE\_TRANSLATECHANGE.</span></span>

 

 
