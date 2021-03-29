---
description: Извлекает целевой объект символьной ссылки.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Функция Нткуерисимболиклинкобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648062"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="cf9a1-103">Функция Нткуерисимболиклинкобжект</span><span class="sxs-lookup"><span data-stu-id="cf9a1-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="cf9a1-104">\[Эта функция может быть изменена или недоступна в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="cf9a1-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cf9a1-105">Извлекает целевой объект символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9a1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf9a1-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="cf9a1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf9a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9a1-108">*Линкхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf9a1-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9a1-109">Маркер объекта символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="cf9a1-110">*LinkTarget* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cf9a1-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9a1-111">Указатель на инициализированную строку Юникода, которая получает целевой объект символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="cf9a1-112">Если вызов завершается неудачей, необходимо задать элементы **MaximumLength** и **buffer** .</span><span class="sxs-lookup"><span data-stu-id="cf9a1-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="cf9a1-113">*Ретурнедленгс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="cf9a1-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9a1-114">Указатель на переменную, которая получает длину строки Юникода, возвращаемую в параметре *LinkTarget* .</span><span class="sxs-lookup"><span data-stu-id="cf9a1-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="cf9a1-115">Если функция возвращает **буфер состояния \_ \_ слишком \_ мал**, эта переменная получает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9a1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf9a1-116">Return value</span></span>

<span data-ttu-id="cf9a1-117">Функция возвращает состояние **\_ Success** или Error.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf9a1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf9a1-118">Remarks</span></span>

<span data-ttu-id="cf9a1-119">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cf9a1-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9a1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cf9a1-120">Requirements</span></span>



| <span data-ttu-id="cf9a1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cf9a1-121">Requirement</span></span> | <span data-ttu-id="cf9a1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cf9a1-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9a1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cf9a1-123">DLL</span></span><br/> | <dl> <span data-ttu-id="cf9a1-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf9a1-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9a1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf9a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9a1-126">**нтопенсимболиклинкобжект**</span><span class="sxs-lookup"><span data-stu-id="cf9a1-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
