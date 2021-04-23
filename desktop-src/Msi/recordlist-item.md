---
description: Свойство Item является свойством, предназначенным только для чтения и возвращающим запись в коллекции объектов Рекордлист.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Рекордлист. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668634"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="89245-103">Рекордлист. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="89245-103">RecordList.Item property</span></span>

<span data-ttu-id="89245-104">Свойство **Item** является свойством, предназначенным только для чтения и возвращающим запись в коллекции объектов [**рекордлист**](recordlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="89245-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="89245-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89245-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89245-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89245-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="89245-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89245-107">Property value</span></span>

<span data-ttu-id="89245-108">Номер индекса элемента с коллекцией строк.</span><span class="sxs-lookup"><span data-stu-id="89245-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="89245-109">Требуется индекс.</span><span class="sxs-lookup"><span data-stu-id="89245-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="89245-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89245-110">Remarks</span></span>

<span data-ttu-id="89245-111">Клиент должен убедиться, что объект [**рекордлист**](recordlist-object.md) существует и не пуст, прежде чем ссылаться на свойство Item.</span><span class="sxs-lookup"><span data-stu-id="89245-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="89245-112">Требования</span><span class="sxs-lookup"><span data-stu-id="89245-112">Requirements</span></span>



| <span data-ttu-id="89245-113">Требование</span><span class="sxs-lookup"><span data-stu-id="89245-113">Requirement</span></span> | <span data-ttu-id="89245-114">Значение</span><span class="sxs-lookup"><span data-stu-id="89245-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89245-115">Версия</span><span class="sxs-lookup"><span data-stu-id="89245-115">Version</span></span><br/> | <span data-ttu-id="89245-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89245-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="89245-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="89245-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="89245-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="89245-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="89245-119">DLL</span><span class="sxs-lookup"><span data-stu-id="89245-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="89245-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89245-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="89245-121">IID</span><span class="sxs-lookup"><span data-stu-id="89245-121">IID</span></span><br/>     | <span data-ttu-id="89245-122">IID \_ ирекордлист определен как 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="89245-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




