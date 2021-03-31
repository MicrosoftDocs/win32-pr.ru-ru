---
description: Функция Хтмлвалуетауникоде преобразует строку HTML CP \_ UTF8 в строку Юникода.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Функция Хтмлвалуетауникоде (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808699"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="a0cde-103">Функция Хтмлвалуетауникоде</span><span class="sxs-lookup"><span data-stu-id="a0cde-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="a0cde-104">Функция **хтмлвалуетауникоде** ПРЕОБРАЗУЕТ строку HTML CP \_ UTF8 в строку Юникода.</span><span class="sxs-lookup"><span data-stu-id="a0cde-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0cde-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a0cde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0cde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0cde-107">*pValue* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a0cde-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0cde-108">На входе указатель на строку HTML, предоставленную МКСВК.</span><span class="sxs-lookup"><span data-stu-id="a0cde-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="a0cde-109">В выходных данных указатель на преобразованную строку Юникода.</span><span class="sxs-lookup"><span data-stu-id="a0cde-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0cde-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0cde-110">Return value</span></span>

<span data-ttu-id="a0cde-111">Функция возвращает эквивалент строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="a0cde-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cde-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a0cde-112">Requirements</span></span>



| <span data-ttu-id="a0cde-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a0cde-113">Requirement</span></span> | <span data-ttu-id="a0cde-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a0cde-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cde-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0cde-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cde-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0cde-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a0cde-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0cde-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cde-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0cde-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a0cde-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a0cde-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0cde-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0cde-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a0cde-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0cde-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0cde-122"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0cde-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0cde-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a0cde-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0cde-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0cde-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




