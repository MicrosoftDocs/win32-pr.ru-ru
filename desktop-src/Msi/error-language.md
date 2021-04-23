---
description: Свойство Language, доступное только для чтения объекта Error, возвращает LANGID текущей ошибки.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Свойство Error. Language (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652043"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="6c7ea-103">Error. Language, свойство</span><span class="sxs-lookup"><span data-stu-id="6c7ea-103">Error.Language property</span></span>

<span data-ttu-id="6c7ea-104">Свойство **Language** , доступное только для чтения объекта [**Error**](error-object.md) , возвращает **LangID** текущей ошибки.</span><span class="sxs-lookup"><span data-stu-id="6c7ea-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="6c7ea-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c7ea-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7ea-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c7ea-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="6c7ea-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6c7ea-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6c7ea-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c7ea-108">Remarks</span></span>

<span data-ttu-id="6c7ea-109">Значение свойства **Language** равно-1, если ошибка не относится к типу Мсмеррорлангуажеунсуппортед или мсмеррорлангуажефаилед.</span><span class="sxs-lookup"><span data-stu-id="6c7ea-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="6c7ea-110">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6c7ea-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="6c7ea-111">C++</span><span class="sxs-lookup"><span data-stu-id="6c7ea-111">C++</span></span>

<span data-ttu-id="6c7ea-112">См. раздел [**Получение \_ языковой функции (объект Error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="6c7ea-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7ea-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6c7ea-113">Requirements</span></span>



| <span data-ttu-id="6c7ea-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6c7ea-114">Requirement</span></span> | <span data-ttu-id="6c7ea-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7ea-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7ea-116">Версия</span><span class="sxs-lookup"><span data-stu-id="6c7ea-116">Version</span></span><br/> | <span data-ttu-id="6c7ea-117">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6c7ea-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6c7ea-118">Header</span><span class="sxs-lookup"><span data-stu-id="6c7ea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c7ea-119"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c7ea-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6c7ea-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c7ea-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

