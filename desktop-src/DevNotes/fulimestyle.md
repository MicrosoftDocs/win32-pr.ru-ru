---
description: Указывает, имеет ли стиль, не являющийся цветом, стиль подчеркивания.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: Функция Фулиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648115"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="f61b3-103">Функция Фулиместиле</span><span class="sxs-lookup"><span data-stu-id="f61b3-103">FUlIMEStyle function</span></span>

<span data-ttu-id="f61b3-104">Указывает, имеет ли стиль, не являющийся цветом, стиль подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="f61b3-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f61b3-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="f61b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f61b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61b3-107">*пиместиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f61b3-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61b3-108">Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="f61b3-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61b3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f61b3-109">Return value</span></span>

<span data-ttu-id="f61b3-110">Значение TRUE, если стиль имеет стиль подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="f61b3-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="f61b3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f61b3-111">Remarks</span></span>

<span data-ttu-id="f61b3-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f61b3-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61b3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f61b3-113">Requirements</span></span>



| <span data-ttu-id="f61b3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f61b3-114">Requirement</span></span> | <span data-ttu-id="f61b3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f61b3-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f61b3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f61b3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f61b3-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61b3-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61b3-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f61b3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61b3-119">**пиместилефроматтр**</span><span class="sxs-lookup"><span data-stu-id="f61b3-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
