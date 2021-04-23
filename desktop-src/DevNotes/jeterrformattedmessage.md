---
description: Извлекает идентификатор кода ошибки (IDA) и создает окончательную строку вывода, когда предоставляется ошибка Jet и расширенные сведения об ошибке.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Функция Жетеррформаттедмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647945"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="8b2fb-103">Функция Жетеррформаттедмессаже</span><span class="sxs-lookup"><span data-stu-id="8b2fb-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="8b2fb-104">Извлекает идентификатор кода ошибки (IDA) и создает окончательную строку вывода, когда предоставляется ошибка Jet и расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b2fb-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="8b2fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b2fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2fb-107">*Err*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-108">Номер ошибки Jet, используемый для поиска и форматирования отображаемого сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-109">*пекстендедерроринфо*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-110">Все сведения об ошибках Jet, включая имя базы данных, имя таблицы и любые незначительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-111">*пида*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-112">Указатель на IDA, связанный с конкретным кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-113">*пмессаже*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-114">Указатель на сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-115">*кбмессаже*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-116">Число байтов в сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-117">*пкбактуал*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-118">Указатель на фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-119">*пконтекстид*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-120">Указатель на идентификатор контекста, связанный с файлом справки.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="8b2fb-121">*Пвсзелп/файл*</span><span class="sxs-lookup"><span data-stu-id="8b2fb-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2fb-122">Указатель на указатель на файл, объясняющий ошибку.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2fb-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b2fb-123">Return value</span></span>

<span data-ttu-id="8b2fb-124">Если функция выполнена успешно, она возвращает значение **Jet \_ еррсукцесс**; в противном случае возвращается отформатированное сообщение об ошибке, указывающее конкретную причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="8b2fb-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b2fb-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b2fb-125">Remarks</span></span>

<span data-ttu-id="8b2fb-126">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8b2fb-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2fb-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8b2fb-127">Requirements</span></span>



| <span data-ttu-id="8b2fb-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8b2fb-128">Requirement</span></span> | <span data-ttu-id="8b2fb-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8b2fb-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2fb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2fb-130">DLL</span></span><br/> | <dl> <span data-ttu-id="8b2fb-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2fb-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
