---
description: Извлекает идентификатор кода ошибки (IDA) и неформатированную строку сообщения, если указана ошибка Jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Функция Жетеррравмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647953"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="6399c-103">Функция Жетеррравмессаже</span><span class="sxs-lookup"><span data-stu-id="6399c-103">JetErrRawMessage function</span></span>

<span data-ttu-id="6399c-104">Извлекает идентификатор кода ошибки (IDA) и неформатированную строку сообщения, если указана ошибка Jet.</span><span class="sxs-lookup"><span data-stu-id="6399c-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="6399c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6399c-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="6399c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6399c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6399c-107">*Err*</span><span class="sxs-lookup"><span data-stu-id="6399c-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-108">Ошибка Jet, соответствующая полученной информации.</span><span class="sxs-lookup"><span data-stu-id="6399c-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-109">*пида*</span><span class="sxs-lookup"><span data-stu-id="6399c-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-110">Указатель на IDA.</span><span class="sxs-lookup"><span data-stu-id="6399c-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-111">*пмессаже*</span><span class="sxs-lookup"><span data-stu-id="6399c-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-112">Указатель на сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6399c-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-113">*кбмессаже*</span><span class="sxs-lookup"><span data-stu-id="6399c-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-114">Число байтов в сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6399c-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-115">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="6399c-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-116">Указатель на фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="6399c-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-117">*пконтекстид*</span><span class="sxs-lookup"><span data-stu-id="6399c-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-118">Указатель на идентификатор контекста, связанный с файлом справки.</span><span class="sxs-lookup"><span data-stu-id="6399c-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="6399c-119">*Пвсзелп/файл*</span><span class="sxs-lookup"><span data-stu-id="6399c-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="6399c-120">Указывает на указатель на файл, объясняющий ошибку.</span><span class="sxs-lookup"><span data-stu-id="6399c-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6399c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6399c-121">Return value</span></span>

<span data-ttu-id="6399c-122">Если функция завершается успешно, она возвращает **Jet \_ еррсукцесс**; в противном случае она возвращает неформатированное сообщение об ошибке, указывающее конкретную причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="6399c-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6399c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6399c-123">Remarks</span></span>

<span data-ttu-id="6399c-124">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6399c-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6399c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6399c-125">Requirements</span></span>



| <span data-ttu-id="6399c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6399c-126">Requirement</span></span> | <span data-ttu-id="6399c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6399c-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6399c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6399c-128">DLL</span></span><br/> | <dl> <span data-ttu-id="6399c-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6399c-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
