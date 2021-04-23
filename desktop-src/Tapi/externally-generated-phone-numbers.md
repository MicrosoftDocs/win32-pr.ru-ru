---
description: Поставщик услуг может указывать внешние номера телефонов, устанавливая элементы структуры ЛИНЕКАЛЛИНФО при обработке \_ функции ЛИНЕЖЕТКАЛЛИНФО тспи.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Внешние созданные номера телефонов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809862"
---
# <a name="externally-generated-phone-numbers"></a><span data-ttu-id="0d1c8-103">Внешние созданные номера телефонов</span><span class="sxs-lookup"><span data-stu-id="0d1c8-103">Externally Generated Phone Numbers</span></span>

<span data-ttu-id="0d1c8-104">Поставщик услуг может указывать на внешние созданные телефонные номера (то есть числа для исходящих вызовов, создаваемых извне на компьютере), задавая элементы **дисплайаблеаддресс**, **калледпарти** или [comment](./comment-ovr.md) в структуре [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo) при обработке функции [**тспи \_ линежеткаллинфо**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="0d1c8-104">A service provider can indicate externally generated phone numbers (that is, numbers for outbound calls generated externally to the computer) by setting the **DisplayableAddress**, **CalledParty**, or [Comment](./comment-ovr.md) members in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure when processing the [**TSPI\_lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) function.</span></span> <span data-ttu-id="0d1c8-105">Если интерфейс TAPI не сохранил собственные данные для этих членов, он оставляет набор данных неизменным для поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0d1c8-105">If TAPI has not saved its own data for these members, it leaves the data set by the service provider unchanged.</span></span> <span data-ttu-id="0d1c8-106">Если у TAPI есть кэшированные данные для этих членов, TAPI добавляет его текст в конец переменной структуры **линекаллинфо** и перезаписывает размер и смещение, помещенные поставщиком службы в фиксированную часть.</span><span class="sxs-lookup"><span data-stu-id="0d1c8-106">If TAPI does have cached data for these members, TAPI adds its text to the end of the variable portion of the **LINECALLINFO** structure and overwrites the size and offset the service provider has put into the fixed portion.</span></span>

<span data-ttu-id="0d1c8-107">Поставщик услуг также может скопировать исходящий номер в элемент **калледид** .</span><span class="sxs-lookup"><span data-stu-id="0d1c8-107">A service provider can also copy an outbound number into the **CalledID** member.</span></span> <span data-ttu-id="0d1c8-108">Поэтому приложения ведения журнала должны проверить элемент **калледид** на исходящих вызовах, если элементы **дисплайаблеаддресс** и **калледпарти** пусты.</span><span class="sxs-lookup"><span data-stu-id="0d1c8-108">Therefore, logging applications should check the **CalledID** member on outbound calls if the **DisplayableAddress** and **CalledParty** members are empty.</span></span>

 

 
