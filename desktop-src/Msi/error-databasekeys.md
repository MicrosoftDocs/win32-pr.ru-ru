---
description: Свойство Датабасекэйс только для чтения объекта Error Возвращает коллекцию строк, содержащую первичные ключи строки базы данных, вызвавшей ошибку. В коллекции имеется один ключ для каждой записи.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Ошибка. свойство Датабасекэйс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651580"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="9ce9d-104">Ошибка. Датабасекэйс, свойство</span><span class="sxs-lookup"><span data-stu-id="9ce9d-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="9ce9d-105">Свойство **датабасекэйс** только для чтения объекта [**Error**](error-object.md) Возвращает коллекцию строк, содержащую первичные ключи строки базы данных, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="9ce9d-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="9ce9d-106">В коллекции имеется один ключ для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9ce9d-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="9ce9d-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9ce9d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ce9d-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="9ce9d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9ce9d-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9ce9d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ce9d-110">Remarks</span></span>

<span data-ttu-id="9ce9d-111">Клиент несет ответственность за освобождение коллекции строк, когда она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="9ce9d-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="9ce9d-112">Если значения не применяются к типу ошибки, коллекция пуста.</span><span class="sxs-lookup"><span data-stu-id="9ce9d-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="9ce9d-113">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce9d-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="9ce9d-114">C++</span><span class="sxs-lookup"><span data-stu-id="9ce9d-114">C++</span></span>

<span data-ttu-id="9ce9d-115">См. раздел [**Получение функции \_ датабасекэйс**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .</span><span class="sxs-lookup"><span data-stu-id="9ce9d-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce9d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce9d-116">Requirements</span></span>



| <span data-ttu-id="9ce9d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce9d-117">Requirement</span></span> | <span data-ttu-id="9ce9d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce9d-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce9d-119">Версия</span><span class="sxs-lookup"><span data-stu-id="9ce9d-119">Version</span></span><br/> | <span data-ttu-id="9ce9d-120">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9ce9d-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="9ce9d-121">Header</span><span class="sxs-lookup"><span data-stu-id="9ce9d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9ce9d-122"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce9d-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ce9d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9ce9d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ce9d-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ce9d-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

