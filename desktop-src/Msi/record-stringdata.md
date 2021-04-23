---
description: Свойство StringData объекта Record — это свойство, доступное для чтения и записи, которое передает строковые данные в указанное поле в записи или из него. Если было сохранено целое число или объект, возвращается его строковое значение.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Свойство Record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668635"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="53740-104">Свойство Record. StringData</span><span class="sxs-lookup"><span data-stu-id="53740-104">Record.StringData property</span></span>

<span data-ttu-id="53740-105">Свойство **StringData** объекта [**Record**](record-object.md) — это свойство, доступное для чтения и записи, которое передает строковые данные в указанное поле в записи или из него.</span><span class="sxs-lookup"><span data-stu-id="53740-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="53740-106">Если было сохранено целое число или объект, возвращается его строковое значение.</span><span class="sxs-lookup"><span data-stu-id="53740-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="53740-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="53740-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53740-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53740-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="53740-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="53740-109">Property value</span></span>

<span data-ttu-id="53740-110">Обязательный номер поля значения в записи, 1.</span><span class="sxs-lookup"><span data-stu-id="53740-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="53740-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53740-111">Remarks</span></span>

<span data-ttu-id="53740-112">Возвращенное значение несуществующего поля является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="53740-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="53740-113">Чтобы задать для поля записи строки значение null, используйте пустой вариант или пустую строку.</span><span class="sxs-lookup"><span data-stu-id="53740-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="53740-114">Попытка сохранить значение в несуществующем поле приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="53740-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="53740-115">Требования</span><span class="sxs-lookup"><span data-stu-id="53740-115">Requirements</span></span>



| <span data-ttu-id="53740-116">Требование</span><span class="sxs-lookup"><span data-stu-id="53740-116">Requirement</span></span> | <span data-ttu-id="53740-117">Значение</span><span class="sxs-lookup"><span data-stu-id="53740-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53740-118">Версия</span><span class="sxs-lookup"><span data-stu-id="53740-118">Version</span></span><br/> | <span data-ttu-id="53740-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53740-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="53740-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="53740-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="53740-121">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="53740-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="53740-122">DLL</span><span class="sxs-lookup"><span data-stu-id="53740-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="53740-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53740-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="53740-124">IID</span><span class="sxs-lookup"><span data-stu-id="53740-124">IID</span></span><br/>     | <span data-ttu-id="53740-125">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="53740-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




