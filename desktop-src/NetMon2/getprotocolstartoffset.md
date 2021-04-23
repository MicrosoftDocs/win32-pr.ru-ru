---
description: Возвращает смещение указанного протокола в кадре.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Функция Жетпротоколстартоффсет (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662183"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="71cc3-103">Функция Жетпротоколстартоффсет</span><span class="sxs-lookup"><span data-stu-id="71cc3-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="71cc3-104">Функция **жетпротоколстартоффсет** возвращает смещение указанного протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="71cc3-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cc3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71cc3-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="71cc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71cc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cc3-107">*хфраме*</span><span class="sxs-lookup"><span data-stu-id="71cc3-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="71cc3-108">Маркер фрейма.</span><span class="sxs-lookup"><span data-stu-id="71cc3-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="71cc3-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="71cc3-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="71cc3-110">Имя протокола, например TCP.</span><span class="sxs-lookup"><span data-stu-id="71cc3-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cc3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71cc3-111">Return value</span></span>

<span data-ttu-id="71cc3-112">Если функция выполнена успешно, возвращаемое значение является смещением **DWORD** до начала протокола, для которого выполняется поиск возвращаемого значения 0 указывает, что протокол является первым протоколом в кадре.</span><span class="sxs-lookup"><span data-stu-id="71cc3-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="71cc3-113">Если функция завершилась неудачно, то протокол не находится в кадре, возвращаемое значение равно-1.</span><span class="sxs-lookup"><span data-stu-id="71cc3-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cc3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71cc3-114">Remarks</span></span>

<span data-ttu-id="71cc3-115">При присвоении маркеру кадра эта функция возвращает смещение к указанному протоколу в кадре.</span><span class="sxs-lookup"><span data-stu-id="71cc3-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="71cc3-116">Например, чтобы определить, является ли кадр кадром DNS, средство синтаксического анализа DNS требует адрес порта протокола TCP.</span><span class="sxs-lookup"><span data-stu-id="71cc3-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="71cc3-117">Средство синтаксического анализа DNS вызовет эту функцию с TCP в качестве значения *ProtocolName* .</span><span class="sxs-lookup"><span data-stu-id="71cc3-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="71cc3-118">Если кадр распознается протоколом TCP, возвращается смещение **слова** от начала кадра до начала кадра TCP.</span><span class="sxs-lookup"><span data-stu-id="71cc3-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="71cc3-119">Если протокол TCP отсутствует, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="71cc3-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="71cc3-120">Эта функция находит начало протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="71cc3-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="71cc3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="71cc3-121">Requirements</span></span>



| <span data-ttu-id="71cc3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="71cc3-122">Requirement</span></span> | <span data-ttu-id="71cc3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="71cc3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71cc3-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71cc3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71cc3-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71cc3-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="71cc3-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71cc3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71cc3-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71cc3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="71cc3-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="71cc3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71cc3-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="71cc3-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="71cc3-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71cc3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="71cc3-131"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71cc3-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="71cc3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="71cc3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71cc3-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71cc3-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




