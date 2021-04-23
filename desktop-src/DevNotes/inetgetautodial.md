---
description: Функция Инетжетаутодиал Возвращает параметры автонабора из реестра.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Функция Инетжетаутодиал
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669069"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="89d03-103">Функция Инетжетаутодиал</span><span class="sxs-lookup"><span data-stu-id="89d03-103">InetGetAutodial function</span></span>

<span data-ttu-id="89d03-104">\[Эта функция не поддерживается и может быть изменена или недоступна в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="89d03-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="89d03-105">\]</span><span class="sxs-lookup"><span data-stu-id="89d03-105">\]</span></span>

<span data-ttu-id="89d03-106">Функция **инетжетаутодиал** Возвращает параметры автонабора из реестра.</span><span class="sxs-lookup"><span data-stu-id="89d03-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d03-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d03-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="89d03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89d03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d03-109">*лпфенабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="89d03-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89d03-110">Указывает, включен ли автонабор.</span><span class="sxs-lookup"><span data-stu-id="89d03-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="89d03-111">Значение **true** при возврате означает, что автонабор включен.</span><span class="sxs-lookup"><span data-stu-id="89d03-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="89d03-112">*лпсзентринаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="89d03-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89d03-113">При возврате содержит имя записи телефонной книги, настроенной для автонабора.</span><span class="sxs-lookup"><span data-stu-id="89d03-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="89d03-114">*кбентринамесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89d03-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89d03-115">Размер буфера, выделенного вызывающим объектом для имени записи телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="89d03-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d03-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89d03-116">Return value</span></span>

<span data-ttu-id="89d03-117">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="89d03-117">This function can return one of these values.</span></span>



| <span data-ttu-id="89d03-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="89d03-118">Return code</span></span>                                                                                                | <span data-ttu-id="89d03-119">Описание</span><span class="sxs-lookup"><span data-stu-id="89d03-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89d03-120"><dt>**Ошибка при \_ успешном выполнении**</dt></span><span class="sxs-lookup"><span data-stu-id="89d03-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="89d03-121">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="89d03-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="89d03-122"><dt>**ошибочные \_ \_ аргументы**</dt></span><span class="sxs-lookup"><span data-stu-id="89d03-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="89d03-123">*лпфенабле* или *лпсзентринаме* содержит **пустой** указатель, или значение *кбентринамесизе* равно нулю.</span><span class="sxs-lookup"><span data-stu-id="89d03-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="89d03-124"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="89d03-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="89d03-125">Недостаточно памяти для выделения внутренних буферов.</span><span class="sxs-lookup"><span data-stu-id="89d03-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="89d03-126"><dt>**Ошибка \_ недостаточного \_ буфера**</dt></span><span class="sxs-lookup"><span data-stu-id="89d03-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="89d03-127">*кбентринамесизе* не указывает, что буфер, на который указывает *лпсзентринаме* , достаточно велик для получения имени записи телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="89d03-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89d03-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89d03-128">Remarks</span></span>

<span data-ttu-id="89d03-129">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="89d03-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d03-130">Требования</span><span class="sxs-lookup"><span data-stu-id="89d03-130">Requirements</span></span>



| <span data-ttu-id="89d03-131">Требование</span><span class="sxs-lookup"><span data-stu-id="89d03-131">Requirement</span></span> | <span data-ttu-id="89d03-132">Значение</span><span class="sxs-lookup"><span data-stu-id="89d03-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89d03-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89d03-133">DLL</span></span><br/> | <dl> <span data-ttu-id="89d03-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d03-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
