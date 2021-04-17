---
description: Это свойство IntegerData объекта Record. Это свойство, доступное для чтения и записи, передает 32-разрядные целочисленные данные в указанное поле в записи или из него. Если значение поля не может быть преобразовано в целое число, возвращается Мсидатабасенуллинтежер.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Свойство Record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651947"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="5b96a-105">Свойство Record. IntegerData</span><span class="sxs-lookup"><span data-stu-id="5b96a-105">Record.IntegerData property</span></span>

<span data-ttu-id="5b96a-106">Это свойство **IntegerData** объекта [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5b96a-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="5b96a-107">Это свойство, доступное для чтения и записи, передает 32-разрядные целочисленные данные в указанное поле в записи или из него.</span><span class="sxs-lookup"><span data-stu-id="5b96a-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="5b96a-108">Если значение поля не может быть преобразовано в целое число, возвращается Мсидатабасенуллинтежер.</span><span class="sxs-lookup"><span data-stu-id="5b96a-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="5b96a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5b96a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b96a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b96a-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5b96a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5b96a-111">Property value</span></span>

<span data-ttu-id="5b96a-112">Обязательный номер поля значения в записи, 1.</span><span class="sxs-lookup"><span data-stu-id="5b96a-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b96a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b96a-113">Remarks</span></span>

<span data-ttu-id="5b96a-114">Чтобы задать для поля записи целое значение null, используйте Мсидатабасенуллинтежер.</span><span class="sxs-lookup"><span data-stu-id="5b96a-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="5b96a-115">Возвращенное значение несуществующего поля — Мсидатабасенуллинтежер.</span><span class="sxs-lookup"><span data-stu-id="5b96a-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="5b96a-116">Попытка сохранить значение в несуществующем поле приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="5b96a-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b96a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5b96a-117">Requirements</span></span>



| <span data-ttu-id="5b96a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5b96a-118">Requirement</span></span> | <span data-ttu-id="5b96a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5b96a-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b96a-120">Версия</span><span class="sxs-lookup"><span data-stu-id="5b96a-120">Version</span></span><br/> | <span data-ttu-id="5b96a-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b96a-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b96a-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b96a-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b96a-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b96a-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5b96a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5b96a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b96a-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b96a-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5b96a-126">IID</span><span class="sxs-lookup"><span data-stu-id="5b96a-126">IID</span></span><br/>     | <span data-ttu-id="5b96a-127">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5b96a-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




