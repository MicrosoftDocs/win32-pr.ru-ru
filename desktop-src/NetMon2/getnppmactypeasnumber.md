---
description: Извлекает тип MAC из категории Нетворкинфо раздела НПП большого двоичного объекта и преобразует данные типа в MAC-тип.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Функция Жетнппмактипеаснумбер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540202"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="b4379-103">Функция Жетнппмактипеаснумбер</span><span class="sxs-lookup"><span data-stu-id="b4379-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="b4379-104">Функция **жетнппмактипеаснумбер** ИЗВЛЕКАЕТ тип Mac из категории нетворкинфо в разделе НПП большого двоичного объекта и преобразует данные типа в Mac-тип.</span><span class="sxs-lookup"><span data-stu-id="b4379-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4379-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4379-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="b4379-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4379-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4379-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4379-108">Маркер указанного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="b4379-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b4379-109">*лпмактипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4379-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4379-110">Указатель на тип MAC.</span><span class="sxs-lookup"><span data-stu-id="b4379-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4379-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4379-111">Return value</span></span>

<span data-ttu-id="b4379-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b4379-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b4379-113">Если тег недоступен, возвращаемое значение имеет \_ тип Mac \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="b4379-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4379-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4379-114">Remarks</span></span>

<span data-ttu-id="b4379-115">Эта функция сопоставляет тег **НПП: нетворкинфо: MacType** с **\_ \_ \* типом Mac** , как определено в файле нпптипес. h.</span><span class="sxs-lookup"><span data-stu-id="b4379-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4379-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b4379-116">Requirements</span></span>



| <span data-ttu-id="b4379-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b4379-117">Requirement</span></span> | <span data-ttu-id="b4379-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b4379-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4379-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4379-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4379-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4379-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b4379-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4379-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4379-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4379-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4379-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4379-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4379-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4379-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b4379-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4379-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4379-126"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4379-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4379-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b4379-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4379-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4379-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




