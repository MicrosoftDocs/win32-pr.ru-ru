---
description: Извлекает значение, определяющее, является ли указанный в памяти или на диске динамический код .NET CRL доверенным для политики Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Функция Влдпкуеридинамиккодетруст (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538753"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="457af-103">Функция Влдпкуеридинамиккодетруст</span><span class="sxs-lookup"><span data-stu-id="457af-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="457af-104">Извлекает значение, определяющее, является ли указанный в памяти или на диске динамический код .NET CRL доверенным для политики Device Guard.</span><span class="sxs-lookup"><span data-stu-id="457af-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="457af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="457af-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="457af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="457af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457af-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="457af-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="457af-108">Обработчик файла динамического кода на диске для проверки.</span><span class="sxs-lookup"><span data-stu-id="457af-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="457af-109">Если *fileHandle* имеет значение, отличное от **null**, *басеимаже* должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="457af-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="457af-110">*басеимаже*</span><span class="sxs-lookup"><span data-stu-id="457af-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="457af-111">Указатель на проверяемый файл PE в памяти.</span><span class="sxs-lookup"><span data-stu-id="457af-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="457af-112">Если *басеимаже* имеет значение, отличное от **null**, *FileHandle* должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="457af-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="457af-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="457af-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="457af-114">Если *басеимаже* имеет значение, отличное от **null**, указывает размер буфера, на который указывает *басеимаже* .</span><span class="sxs-lookup"><span data-stu-id="457af-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="457af-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="457af-115">Return value</span></span>

<span data-ttu-id="457af-116">Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="457af-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="457af-117">Требования</span><span class="sxs-lookup"><span data-stu-id="457af-117">Requirements</span></span>



| <span data-ttu-id="457af-118">Требование</span><span class="sxs-lookup"><span data-stu-id="457af-118">Requirement</span></span> | <span data-ttu-id="457af-119">Значение</span><span class="sxs-lookup"><span data-stu-id="457af-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="457af-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="457af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="457af-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="457af-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="457af-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="457af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="457af-123">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="457af-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="457af-124">Header</span><span class="sxs-lookup"><span data-stu-id="457af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="457af-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="457af-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="457af-126">DLL</span><span class="sxs-lookup"><span data-stu-id="457af-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="457af-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="457af-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




