---
description: Значение свойства сводка субъекта передает имя продукта, преобразование или исправление, установленное пакетом.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Свойство сводки субъекта
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651836"
---
# <a name="subject-summary-property"></a><span data-ttu-id="364b4-103">Свойство сводки субъекта</span><span class="sxs-lookup"><span data-stu-id="364b4-103">Subject Summary property</span></span>

<span data-ttu-id="364b4-104">Значение свойства **Сводка субъекта** передает имя продукта, преобразование или исправление, установленное пакетом.</span><span class="sxs-lookup"><span data-stu-id="364b4-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="364b4-105">Вы должны быть автором базы данных установки, преобразованием или пакетом исправлений, чтобы предоставить значение этого свойства в сводных данных.</span><span class="sxs-lookup"><span data-stu-id="364b4-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="364b4-106">Авторы должны выполнить следующие действия, чтобы определить правильное значение.</span><span class="sxs-lookup"><span data-stu-id="364b4-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="364b4-107">Задайте для свойства **Сводка субъекта** в пакете установки то же значение, что и у свойства [**ProductName**](productname.md) .</span><span class="sxs-lookup"><span data-stu-id="364b4-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="364b4-108">Задайте для свойства **Сводка субъекта** в преобразовании то же значение, что и в свойстве **Сводка субъекта** в исходном пакете установки.</span><span class="sxs-lookup"><span data-stu-id="364b4-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="364b4-109">Задайте для свойства **Сводка субъекта** в сводных данных пакета исправлений краткое описание исправления, которое содержит имя продукта.</span><span class="sxs-lookup"><span data-stu-id="364b4-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="364b4-110">Требования</span><span class="sxs-lookup"><span data-stu-id="364b4-110">Requirements</span></span>



| <span data-ttu-id="364b4-111">Требование</span><span class="sxs-lookup"><span data-stu-id="364b4-111">Requirement</span></span> | <span data-ttu-id="364b4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="364b4-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="364b4-113">Версия</span><span class="sxs-lookup"><span data-stu-id="364b4-113">Version</span></span><br/> | <span data-ttu-id="364b4-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="364b4-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="364b4-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="364b4-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="364b4-116">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="364b4-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="364b4-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="364b4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="364b4-118">**патчневсуммарисубжект**</span><span class="sxs-lookup"><span data-stu-id="364b4-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="364b4-119">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="364b4-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




