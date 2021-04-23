---
description: Указывает, имеет ли стиль, не являющийся цветом, стиль курсивом.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Функция ФиталиЦиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648855"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="74f7e-103">Функция ФиталиЦиместиле</span><span class="sxs-lookup"><span data-stu-id="74f7e-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="74f7e-104">Указывает, имеет ли стиль, не являющийся цветом, стиль курсивом.</span><span class="sxs-lookup"><span data-stu-id="74f7e-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74f7e-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="74f7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74f7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f7e-107">*пиместиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74f7e-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74f7e-108">Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="74f7e-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f7e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74f7e-109">Return value</span></span>

<span data-ttu-id="74f7e-110">**Значение true** , если стиль имеет курсив.</span><span class="sxs-lookup"><span data-stu-id="74f7e-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f7e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74f7e-111">Remarks</span></span>

<span data-ttu-id="74f7e-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="74f7e-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f7e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="74f7e-113">Requirements</span></span>



| <span data-ttu-id="74f7e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="74f7e-114">Requirement</span></span> | <span data-ttu-id="74f7e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="74f7e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74f7e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="74f7e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="74f7e-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74f7e-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f7e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74f7e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f7e-119">**пиместилефроматтр**</span><span class="sxs-lookup"><span data-stu-id="74f7e-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
