---
description: Функция Креатенппинтерфаце использует большой двоичный объект, возвращенный из Finder, для создания НПП, который может использоваться приложением.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Функция Креатенппинтерфаце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998787"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="c3842-103">Функция Креатенппинтерфаце</span><span class="sxs-lookup"><span data-stu-id="c3842-103">CreateNPPInterface function</span></span>

<span data-ttu-id="c3842-104">Функция **креатенппинтерфаце** использует большой двоичный объект, возвращенный из Finder, для создания НПП, который может использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="c3842-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3842-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3842-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="c3842-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3842-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3842-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3842-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3842-108">Обработчик для большого двоичного объекта, возвращенного из Finder.</span><span class="sxs-lookup"><span data-stu-id="c3842-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="c3842-109">*IID* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c3842-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3842-110">Идентификатор интерфейса, который вызывается из НПП (например,**ИРТК** или **иделайдк**).</span><span class="sxs-lookup"><span data-stu-id="c3842-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="c3842-111">*ппвобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3842-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3842-112">Указатель на возвращаемый указатель на запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c3842-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3842-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3842-113">Return value</span></span>

<span data-ttu-id="c3842-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c3842-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c3842-115">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3842-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3842-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c3842-116">Requirements</span></span>



| <span data-ttu-id="c3842-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c3842-117">Requirement</span></span> | <span data-ttu-id="c3842-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c3842-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3842-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3842-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3842-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3842-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c3842-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3842-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3842-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3842-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3842-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c3842-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3842-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3842-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c3842-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3842-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3842-126"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3842-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3842-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c3842-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3842-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3842-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




