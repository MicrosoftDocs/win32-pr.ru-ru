---
description: Функция Жетпротоколинфо возвращает указатель на значение сведений о протоколе.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Функция Жетпротоколинфо (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990895"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="f27ed-103">Функция Жетпротоколинфо</span><span class="sxs-lookup"><span data-stu-id="f27ed-103">GetProtocolInfo function</span></span>

<span data-ttu-id="f27ed-104">Функция **жетпротоколинфо** возвращает указатель на значение сведений о протоколе.</span><span class="sxs-lookup"><span data-stu-id="f27ed-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f27ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f27ed-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="f27ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f27ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f27ed-107">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f27ed-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f27ed-108">Обработчик для протокола.</span><span class="sxs-lookup"><span data-stu-id="f27ed-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f27ed-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f27ed-109">Return value</span></span>

<span data-ttu-id="f27ed-110">Если функция выполнена успешно, возвращаемое значение является указателем на значение сведений о протоколе.</span><span class="sxs-lookup"><span data-stu-id="f27ed-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="f27ed-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f27ed-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f27ed-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f27ed-112">Remarks</span></span>

<span data-ttu-id="f27ed-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпротоколинфо** .</span><span class="sxs-lookup"><span data-stu-id="f27ed-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f27ed-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f27ed-114">Requirements</span></span>



| <span data-ttu-id="f27ed-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f27ed-115">Requirement</span></span> | <span data-ttu-id="f27ed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f27ed-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f27ed-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f27ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f27ed-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f27ed-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f27ed-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f27ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f27ed-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f27ed-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f27ed-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f27ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f27ed-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f27ed-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f27ed-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f27ed-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f27ed-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f27ed-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f27ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f27ed-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f27ed-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f27ed-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




