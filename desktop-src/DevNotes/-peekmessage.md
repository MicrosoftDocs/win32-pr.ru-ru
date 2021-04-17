---
description: Отправляет входящие отправленные сообщения, проверяет очередь сообщений потока на наличие отправленного сообщения и получает сообщение (если оно существует).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Функция _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648021"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="9f679-103">\_Функция PeekMessage</span><span class="sxs-lookup"><span data-stu-id="9f679-103">\_PeekMessage function</span></span>

<span data-ttu-id="9f679-104">\[Эта функция является оболочкой для функции **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="9f679-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="9f679-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="9f679-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="9f679-106">Приложения должны вызывать **PeekMessage** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="9f679-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="9f679-107">Отправляет входящие отправленные сообщения, проверяет очередь сообщений потока на наличие отправленного сообщения и получает сообщение (если оно существует).</span><span class="sxs-lookup"><span data-stu-id="9f679-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="9f679-108">См. [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="9f679-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f679-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f679-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="9f679-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f679-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f679-111">*...*</span><span class="sxs-lookup"><span data-stu-id="9f679-111">*...*</span></span> 
<span data-ttu-id="9f679-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9f679-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9f679-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9f679-113">Requirements</span></span>



| <span data-ttu-id="9f679-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9f679-114">Requirement</span></span> | <span data-ttu-id="9f679-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9f679-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f679-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9f679-116">DLL</span></span><br/> | <dl> <span data-ttu-id="9f679-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f679-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f679-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f679-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f679-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="9f679-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
