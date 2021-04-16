---
description: Для пакета установки свойство сводка номера редакции содержит код пакета для пакета установщика.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Свойство сводки номеров редакций
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652179"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="64867-103">Свойство сводки номеров редакций</span><span class="sxs-lookup"><span data-stu-id="64867-103">Revision Number Summary property</span></span>

<span data-ttu-id="64867-104">Для пакета установки свойство **Сводка номера редакции** содержит [*код пакета*](p-gly.md) для пакета установщика.</span><span class="sxs-lookup"><span data-stu-id="64867-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="64867-105">Дополнительные сведения о кодах пакетов см. в разделе [коды пакетов](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="64867-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="64867-106">Для преобразования в свойстве **Сводка номера редакции** перечислены идентификаторы GUID и версия новых и исходных продуктов, а также идентификатор GUID кода обновления.</span><span class="sxs-lookup"><span data-stu-id="64867-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="64867-107">Список отделяется точкой с запятой следующим образом.</span><span class="sxs-lookup"><span data-stu-id="64867-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="64867-108">Исходный продукт исходного кода — версия продукта; New-Product код New — версия продукта; Обновление кода "</span><span class="sxs-lookup"><span data-stu-id="64867-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="64867-109">Для пакета исправлений свойство **Сводка номера редакции** указывает код исправления GUID для исправления.</span><span class="sxs-lookup"><span data-stu-id="64867-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="64867-110">За этим может следовать список идентификаторов GUID кода исправления для устаревших исправлений, которые будут удалены после применения этого исправления.</span><span class="sxs-lookup"><span data-stu-id="64867-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="64867-111">Коды исправлений объединяются без разделителей, разделяющих идентификаторы GUID в списке.</span><span class="sxs-lookup"><span data-stu-id="64867-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="64867-112">\* \* Установщик Windows 3,0: \* \* Если в [таблице мсипатчсекуенце](msipatchsequence-table.md)содержится информация о последовательности, установщик Windows 3,0 использует сведения о последовательности в таблице и игнорирует список устаревших исправлений, включенных в свойство **сводки номеров редакций** .</span><span class="sxs-lookup"><span data-stu-id="64867-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="64867-113">Установщик Windows 3,0 по-прежнему может использовать устаревшие сведения об исправлениях в свойстве **сводки номеров редакций** , если пакет не содержит таблицу мсипатчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="64867-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="64867-114">\* \* Установщик Windows 2,0: \* \* [Таблица мсипатчсекуенце](msipatchsequence-table.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="64867-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="64867-115">Установщик Windows 2,0 по-прежнему может использовать устаревшие сведения об исправлениях в свойстве **сводки номеров редакций** , если пакет не содержит таблицу мсипатчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="64867-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="64867-116">Это свойство сводки является обязательным.</span><span class="sxs-lookup"><span data-stu-id="64867-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="64867-117">Требования</span><span class="sxs-lookup"><span data-stu-id="64867-117">Requirements</span></span>



| <span data-ttu-id="64867-118">Требование</span><span class="sxs-lookup"><span data-stu-id="64867-118">Requirement</span></span> | <span data-ttu-id="64867-119">Значение</span><span class="sxs-lookup"><span data-stu-id="64867-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64867-120">Версия</span><span class="sxs-lookup"><span data-stu-id="64867-120">Version</span></span><br/> | <span data-ttu-id="64867-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64867-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64867-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64867-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64867-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="64867-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64867-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64867-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64867-125">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="64867-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




