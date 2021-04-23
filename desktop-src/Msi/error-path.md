---
description: В установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой. Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Свойство Error. Path (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685308"
---
# <a name="errorpath-property"></a><span data-ttu-id="5dc89-104">Свойство Error. Path</span><span class="sxs-lookup"><span data-stu-id="5dc89-104">Error.Path property</span></span>

<span data-ttu-id="5dc89-105">В установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="5dc89-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="5dc89-106">Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.</span><span class="sxs-lookup"><span data-stu-id="5dc89-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="5dc89-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5dc89-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dc89-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="5dc89-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5dc89-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc89-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dc89-110">Remarks</span></span>

<span data-ttu-id="5dc89-111">Это значение допустимо только для ошибок типа Мсмеррорфилекреате или Мсмеррордиркреате.</span><span class="sxs-lookup"><span data-stu-id="5dc89-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="5dc89-112">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc89-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="5dc89-113">C++</span><span class="sxs-lookup"><span data-stu-id="5dc89-113">C++</span></span>

<span data-ttu-id="5dc89-114">См. раздел [**Получение \_ пути**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) функции.</span><span class="sxs-lookup"><span data-stu-id="5dc89-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc89-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5dc89-115">Requirements</span></span>



| <span data-ttu-id="5dc89-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5dc89-116">Requirement</span></span> | <span data-ttu-id="5dc89-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc89-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc89-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5dc89-118">Version</span></span><br/> | <span data-ttu-id="5dc89-119">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5dc89-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5dc89-120">Header</span><span class="sxs-lookup"><span data-stu-id="5dc89-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5dc89-121"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc89-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dc89-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc89-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5dc89-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc89-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

