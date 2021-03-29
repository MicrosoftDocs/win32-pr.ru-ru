---
description: Добавляет строку и дополнительные данные в таблицу.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: Функция Псетупстрингтаблеаддстринжекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665412"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="d4f83-103">Функция Псетупстрингтаблеаддстринжекс</span><span class="sxs-lookup"><span data-stu-id="d4f83-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="d4f83-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="d4f83-105">Добавляет строку и дополнительные данные в таблицу.</span><span class="sxs-lookup"><span data-stu-id="d4f83-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f83-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4f83-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="d4f83-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4f83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f83-108">*STRINGTABLE* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f83-109">Указатель на таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="d4f83-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="d4f83-110">*Строка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f83-111">Указатель на строку, добавляемую в таблицу.</span><span class="sxs-lookup"><span data-stu-id="d4f83-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="d4f83-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f83-113">Значение этого параметра может быть равно `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="d4f83-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="d4f83-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f83-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="d4f83-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f83-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="d4f83-116"><dt>**Стртаб \_ 0x001 \_ с учетом регистра**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d4f83-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="d4f83-117">В строке учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="d4f83-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="d4f83-118"><dt>**Стртаб \_ НОВЫЙ \_ екстрадата**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="d4f83-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="d4f83-119">Имеются дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="d4f83-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="d4f83-120">*Екстрадата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f83-121">Необязательный указатель на дополнительный объект данных.</span><span class="sxs-lookup"><span data-stu-id="d4f83-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="d4f83-122">*Екстрадатасизе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d4f83-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f83-123">Размер дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="d4f83-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4f83-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4f83-124">Remarks</span></span>

<span data-ttu-id="d4f83-125">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d4f83-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f83-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d4f83-126">Requirements</span></span>



| <span data-ttu-id="d4f83-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d4f83-127">Requirement</span></span> | <span data-ttu-id="d4f83-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f83-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f83-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f83-129">DLL</span></span><br/> | <dl> <span data-ttu-id="d4f83-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4f83-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
