---
description: Последнее сохраненное свойство сводки времени/даты передает время, когда этот пакет установки, преобразование или пакет исправлений был modified.Iniтиалли, автор должен установить значение последнего сохраненного свойства "Дата/время" со значением "null", чтобы указать, что в пакет еще не внесены изменения. После этого автор должен обновить последнее сохраненное свойство сводки по дате и времени на текущее системное время и дату при каждом сохранении измененного пакета базы данных установки, преобразования или исправления.
ms.assetid: be3957fa-463a-4eb2-8b9d-93a16e95a8cf
title: Свойство сводки даты и времени последнего сохранения
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe2300640434a52a78575221dc69e0f7263883
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689087"
---
# <a name="last-saved-timedate-summary-property"></a><span data-ttu-id="4856f-104">Свойство сводки даты и времени последнего сохранения</span><span class="sxs-lookup"><span data-stu-id="4856f-104">Last Saved Time/Date Summary property</span></span>

<span data-ttu-id="4856f-105">**Последнее сохраненное свойство сводки времени и дат** передает время последнего изменения пакета установки, преобразования или пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="4856f-105">The **Last Saved Time/Date Summary** property conveys the last time when this installation package, transform, or patch package was modified.</span></span>

<span data-ttu-id="4856f-106">Изначально автор должен присвоить **последнему сохраненному свойству «время/Дата** » значение null, чтобы указать, что в пакет еще не было внесено никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="4856f-106">Initially, an author should set the value of the **Last Saved Time/Date Summary** property to Null to indicate that no changes have yet been made to the package.</span></span> <span data-ttu-id="4856f-107">После этого автор должен обновить **последнее сохраненное свойство сводки по дате и времени** на текущее системное время и дату при каждом сохранении измененного пакета базы данных установки, преобразования или исправления.</span><span class="sxs-lookup"><span data-stu-id="4856f-107">An author should then update the **Last Saved Time/Date Summary** property to the current system time/date each time a modified installation database, transform, or patch package is saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="4856f-108">Требования</span><span class="sxs-lookup"><span data-stu-id="4856f-108">Requirements</span></span>



| <span data-ttu-id="4856f-109">Требование</span><span class="sxs-lookup"><span data-stu-id="4856f-109">Requirement</span></span> | <span data-ttu-id="4856f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4856f-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4856f-111">Версия</span><span class="sxs-lookup"><span data-stu-id="4856f-111">Version</span></span><br/> | <span data-ttu-id="4856f-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4856f-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4856f-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4856f-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4856f-114">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="4856f-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4856f-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4856f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4856f-116">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="4856f-116">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




