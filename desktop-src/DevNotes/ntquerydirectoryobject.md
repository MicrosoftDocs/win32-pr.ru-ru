---
description: Извлекает сведения об указанном объекте каталога.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Функция Нткуеридиректорйобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648063"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="534d7-103">Функция Нткуеридиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="534d7-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="534d7-104">\[Эта функция может быть изменена или недоступна в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="534d7-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="534d7-105">Извлекает сведения об указанном объекте каталога.</span><span class="sxs-lookup"><span data-stu-id="534d7-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="534d7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="534d7-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="534d7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="534d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534d7-108">*Директорихандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="534d7-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-109">Маркер объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="534d7-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-110">*Буфер* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="534d7-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-111">Указатель на буфер, который получает сведения о каталоге.</span><span class="sxs-lookup"><span data-stu-id="534d7-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="534d7-112">Этот буфер получает одну или несколько **\_ \_ информационных структур каталога объектов** , последний из которых **равен null**, а затем строки, содержащие имена записей каталога.</span><span class="sxs-lookup"><span data-stu-id="534d7-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="534d7-113">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="534d7-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-114">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="534d7-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-115">Размер предоставляемого пользователем выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="534d7-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-116">*Ретурнсинглинтри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="534d7-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-117">Указывает, должна ли функция возвращать только одну запись.</span><span class="sxs-lookup"><span data-stu-id="534d7-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-118">*Рестартскан* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="534d7-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-119">Указывает, следует ли перезапустить сканирование или продолжить перечисление, используя сведения, переданные в параметре *контекста* .</span><span class="sxs-lookup"><span data-stu-id="534d7-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-120">*Контекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="534d7-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-121">Контекст перечисления.</span><span class="sxs-lookup"><span data-stu-id="534d7-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="534d7-122">*Ретурнленгс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="534d7-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="534d7-123">Указатель на переменную, которая получает длину сведений о каталоге, возвращаемых в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="534d7-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534d7-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="534d7-124">Return value</span></span>

<span data-ttu-id="534d7-125">Функция возвращает состояние **\_ Success** или Error.</span><span class="sxs-lookup"><span data-stu-id="534d7-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="534d7-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="534d7-126">Remarks</span></span>

<span data-ttu-id="534d7-127">Ниже приведено определение **\_ \_ информационной структуры каталога объектов** .</span><span class="sxs-lookup"><span data-stu-id="534d7-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="534d7-128">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="534d7-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="534d7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="534d7-129">Requirements</span></span>



| <span data-ttu-id="534d7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="534d7-130">Requirement</span></span> | <span data-ttu-id="534d7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="534d7-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="534d7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="534d7-132">DLL</span></span><br/> | <dl> <span data-ttu-id="534d7-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="534d7-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534d7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="534d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534d7-135">**нтопендиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="534d7-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
