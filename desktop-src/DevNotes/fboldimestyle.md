---
description: Указывает, имеет ли стиль, отличный от цвета, полужирный стиль.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: Функция Фболдиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648969"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="19a19-103">Функция Фболдиместиле</span><span class="sxs-lookup"><span data-stu-id="19a19-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="19a19-104">Указывает, имеет ли стиль, отличный от цвета, полужирный стиль.</span><span class="sxs-lookup"><span data-stu-id="19a19-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19a19-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="19a19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a19-107">*пиместиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19a19-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a19-108">Структура **иместиле** , возвращаемая функцией [**пиместилефроматтр**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="19a19-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a19-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19a19-109">Return value</span></span>

<span data-ttu-id="19a19-110">**Значение true** , если стиль имеет полужирный стиль.</span><span class="sxs-lookup"><span data-stu-id="19a19-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a19-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19a19-111">Remarks</span></span>

<span data-ttu-id="19a19-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="19a19-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a19-113">Требования</span><span class="sxs-lookup"><span data-stu-id="19a19-113">Requirements</span></span>



| <span data-ttu-id="19a19-114">Требование</span><span class="sxs-lookup"><span data-stu-id="19a19-114">Requirement</span></span> | <span data-ttu-id="19a19-115">Значение</span><span class="sxs-lookup"><span data-stu-id="19a19-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19a19-116">DLL</span><span class="sxs-lookup"><span data-stu-id="19a19-116">DLL</span></span><br/> | <dl> <span data-ttu-id="19a19-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19a19-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a19-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19a19-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a19-119">**пиместилефроматтр**</span><span class="sxs-lookup"><span data-stu-id="19a19-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
