---
UID: ''
title: Функция Уникодетобитес
description: Преобразует символы Юникода в кодировку GB18030 байт.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "103785490"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="a995e-103">Функция Уникодетобитес</span><span class="sxs-lookup"><span data-stu-id="a995e-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="a995e-104">Описание</span><span class="sxs-lookup"><span data-stu-id="a995e-104">Description</span></span>

<span data-ttu-id="a995e-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a995e-105">Deprecated.</span></span> <span data-ttu-id="a995e-106">Преобразует символы Юникода в кодировку GB18030 байт.</span><span class="sxs-lookup"><span data-stu-id="a995e-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="a995e-107">**Примечание**  .  При преобразовании символов Юникода в кодировку GB18030 байты приложение, запускаемое в Windows Vista и более поздних версиях, должно использовать функцию [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .</span><span class="sxs-lookup"><span data-stu-id="a995e-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="a995e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a995e-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="a995e-109">Лпвидечарстр [in]</span><span class="sxs-lookup"><span data-stu-id="a995e-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="a995e-110">Указатель на строку в Юникоде для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a995e-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="a995e-111">Кчвидечар [in]</span><span class="sxs-lookup"><span data-stu-id="a995e-111">cchWideChar [in]</span></span>

<span data-ttu-id="a995e-112">Число символов в строке Юникода для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a995e-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="a995e-113">Лпмултибитестр [in]</span><span class="sxs-lookup"><span data-stu-id="a995e-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="a995e-114">Указатель на целевой многобайтовый буфер.</span><span class="sxs-lookup"><span data-stu-id="a995e-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="a995e-115">Если *лпмултибитестр* имеет значение 0, возвращается число байтов в результатах GB18030 и преобразование не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a995e-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="a995e-116">Кчмултибите [in]</span><span class="sxs-lookup"><span data-stu-id="a995e-116">cchMultiByte [in]</span></span>

<span data-ttu-id="a995e-117">Число байтов целевого многобайтового буфера.</span><span class="sxs-lookup"><span data-stu-id="a995e-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="a995e-118">Если *кчмултибите* имеет значение 0, возвращается число байтов в результатах GB18030 и преобразование не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a995e-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="a995e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a995e-119">Returns</span></span>

<span data-ttu-id="a995e-120">Возвращает количество байтов многобайтовых символов, создаваемых в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="a995e-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a995e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a995e-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="a995e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a995e-122">See also</span></span>

[<span data-ttu-id="a995e-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="a995e-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="a995e-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="a995e-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
