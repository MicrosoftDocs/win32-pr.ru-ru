---
description: Свойство Модулекэйс только для чтения объекта Error возвращает указатель на коллекцию строк, содержащую первичные ключи строки в модуле, вызвавшей ошибку, по одному ключу на запись в коллекции.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Ошибка. свойство Модулекэйс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651746"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="b197e-103">Ошибка. Модулекэйс, свойство</span><span class="sxs-lookup"><span data-stu-id="b197e-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="b197e-104">Свойство **модулекэйс** только для чтения объекта [**Error**](error-object.md) возвращает указатель на коллекцию строк, содержащую первичные ключи строки в модуле, вызвавшей ошибку, по одному ключу на запись в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b197e-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="b197e-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b197e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b197e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b197e-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="b197e-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b197e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b197e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b197e-108">Remarks</span></span>

<span data-ttu-id="b197e-109">Клиент несет ответственность за освобождение коллекции строк, когда она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="b197e-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="b197e-110">Если значения не применяются к типу ошибки, коллекция пуста.</span><span class="sxs-lookup"><span data-stu-id="b197e-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="b197e-111">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b197e-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="b197e-112">C++</span><span class="sxs-lookup"><span data-stu-id="b197e-112">C++</span></span>

<span data-ttu-id="b197e-113">См. раздел [**Получение функции \_ модулекэйс**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) .</span><span class="sxs-lookup"><span data-stu-id="b197e-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b197e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b197e-114">Requirements</span></span>



| <span data-ttu-id="b197e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b197e-115">Requirement</span></span> | <span data-ttu-id="b197e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b197e-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b197e-117">Версия</span><span class="sxs-lookup"><span data-stu-id="b197e-117">Version</span></span><br/> | <span data-ttu-id="b197e-118">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b197e-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b197e-119">Header</span><span class="sxs-lookup"><span data-stu-id="b197e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b197e-120"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b197e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b197e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b197e-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

