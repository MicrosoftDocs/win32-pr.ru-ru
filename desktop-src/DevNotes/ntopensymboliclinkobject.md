---
description: Открывает существующую символьную ссылку.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Функция Нтопенсимболиклинкобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668693"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="17588-103">Функция Нтопенсимболиклинкобжект</span><span class="sxs-lookup"><span data-stu-id="17588-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="17588-104">\[Эта функция может быть изменена или недоступна в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="17588-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="17588-105">Открывает существующую символьную ссылку.</span><span class="sxs-lookup"><span data-stu-id="17588-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="17588-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17588-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="17588-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="17588-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17588-108">*Линкхандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17588-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17588-109">Маркер вновь открытого объекта символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="17588-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="17588-110">*Десиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17588-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17588-111">[**\_ Маска доступа**](../secauthz/access-mask.md) , указывающая запрошенный доступ к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="17588-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="17588-112">Обычно используется универсальный метод Read, \_ поэтому этот обработчик может быть передан в функцию [**нткуеридиректорйобжект**](ntquerydirectoryobject.md) .</span><span class="sxs-lookup"><span data-stu-id="17588-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="17588-113">*Обжектаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17588-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17588-114">Атрибуты для объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="17588-114">The attributes for the directory object.</span></span> <span data-ttu-id="17588-115">Чтобы инициализировать структуру **\_ атрибутов объекта** , используйте макрос **инитиализеобжектаттрибутес** .</span><span class="sxs-lookup"><span data-stu-id="17588-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="17588-116">Если вызывающий объект не выполняется в системном контексте потока, он должен указать флаг " **obj \_ kernel \_ Handle** " при инициализации структуры.</span><span class="sxs-lookup"><span data-stu-id="17588-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="17588-117">Дополнительные сведения см. в документации по этим элементам в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="17588-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17588-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17588-118">Return value</span></span>

<span data-ttu-id="17588-119">Функция возвращает состояние **\_ Success** или Error.</span><span class="sxs-lookup"><span data-stu-id="17588-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="17588-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17588-120">Remarks</span></span>

<span data-ttu-id="17588-121">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="17588-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="17588-122">Требования</span><span class="sxs-lookup"><span data-stu-id="17588-122">Requirements</span></span>



| <span data-ttu-id="17588-123">Требование</span><span class="sxs-lookup"><span data-stu-id="17588-123">Requirement</span></span> | <span data-ttu-id="17588-124">Значение</span><span class="sxs-lookup"><span data-stu-id="17588-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17588-125">DLL</span><span class="sxs-lookup"><span data-stu-id="17588-125">DLL</span></span><br/> | <dl> <span data-ttu-id="17588-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17588-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17588-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17588-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17588-128">**нткуеридиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="17588-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
