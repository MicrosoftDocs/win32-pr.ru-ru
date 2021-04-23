---
description: Свойство Датабасетабле только для чтения объекта Error возвращает имя таблицы в базе данных, вызвавшей ошибку.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Ошибка. свойство Датабасетабле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651579"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="aacad-103">Ошибка. Датабасетабле, свойство</span><span class="sxs-lookup"><span data-stu-id="aacad-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="aacad-104">Свойство **датабасетабле** только для чтения объекта [**Error**](error-object.md) возвращает имя таблицы в базе данных, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="aacad-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="aacad-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aacad-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aacad-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="aacad-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aacad-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="aacad-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aacad-108">Remarks</span></span>

<span data-ttu-id="aacad-109">Если значения не применяются к типу ошибки, коллекция пуста.</span><span class="sxs-lookup"><span data-stu-id="aacad-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="aacad-110">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="aacad-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="aacad-111">C++</span><span class="sxs-lookup"><span data-stu-id="aacad-111">C++</span></span>

<span data-ttu-id="aacad-112">См. раздел [**Получение функции \_ датабасетабле**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .</span><span class="sxs-lookup"><span data-stu-id="aacad-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aacad-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aacad-113">Requirements</span></span>



| <span data-ttu-id="aacad-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aacad-114">Requirement</span></span> | <span data-ttu-id="aacad-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aacad-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aacad-116">Версия</span><span class="sxs-lookup"><span data-stu-id="aacad-116">Version</span></span><br/> | <span data-ttu-id="aacad-117">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="aacad-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="aacad-118">Header</span><span class="sxs-lookup"><span data-stu-id="aacad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aacad-119"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="aacad-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="aacad-120">DLL</span><span class="sxs-lookup"><span data-stu-id="aacad-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="aacad-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aacad-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

