---
description: Извлекает неформатированную строку сообщения, если указан идентификатор кода ошибки (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Функция Жетерридаравмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669214"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="92c6e-103">Функция Жетерридаравмессаже</span><span class="sxs-lookup"><span data-stu-id="92c6e-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="92c6e-104">Извлекает неформатированную строку сообщения, если указан идентификатор кода ошибки (IDA).</span><span class="sxs-lookup"><span data-stu-id="92c6e-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c6e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92c6e-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="92c6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c6e-107">*IDA*</span><span class="sxs-lookup"><span data-stu-id="92c6e-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-108">Число, сопоставляемое с конкретным кодом ошибки и отображаемое пользователю.</span><span class="sxs-lookup"><span data-stu-id="92c6e-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="92c6e-109">*пмессаже*</span><span class="sxs-lookup"><span data-stu-id="92c6e-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-110">Указатель на сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="92c6e-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="92c6e-111">*кбмессаже*</span><span class="sxs-lookup"><span data-stu-id="92c6e-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-112">Число байтов в сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="92c6e-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="92c6e-113">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="92c6e-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-114">Указатель на фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="92c6e-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="92c6e-115">*пконтекстид*</span><span class="sxs-lookup"><span data-stu-id="92c6e-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-116">Указатель на идентификатор контекста, связанный с файлом справки.</span><span class="sxs-lookup"><span data-stu-id="92c6e-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="92c6e-117">*Пвсзелп/файл*</span><span class="sxs-lookup"><span data-stu-id="92c6e-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6e-118">Указатель на указатель на файл, объясняющий ошибку.</span><span class="sxs-lookup"><span data-stu-id="92c6e-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c6e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92c6e-119">Return value</span></span>

<span data-ttu-id="92c6e-120">Если функция завершается успешно, она возвращает значение **Jet \_ еррсукцесс**; в противном случае возвращается неформатированное сообщение, указывающее конкретную причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="92c6e-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c6e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92c6e-121">Remarks</span></span>

<span data-ttu-id="92c6e-122">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="92c6e-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c6e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="92c6e-123">Requirements</span></span>



| <span data-ttu-id="92c6e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="92c6e-124">Requirement</span></span> | <span data-ttu-id="92c6e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="92c6e-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c6e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="92c6e-126">DLL</span></span><br/> | <dl> <span data-ttu-id="92c6e-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c6e-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
