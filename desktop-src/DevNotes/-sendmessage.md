---
description: Отправляет указанное сообщение в окно или в окна.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Функция _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648020"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="8f06a-103">\_SendMessage, функция</span><span class="sxs-lookup"><span data-stu-id="8f06a-103">\_SendMessage function</span></span>

<span data-ttu-id="8f06a-104">\[Эта функция является оболочкой для функции **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="8f06a-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="8f06a-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="8f06a-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="8f06a-106">Приложения должны вызывать **SendMessage** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="8f06a-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="8f06a-107">Отправляет указанное сообщение в окно или в окна.</span><span class="sxs-lookup"><span data-stu-id="8f06a-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="8f06a-108">См. раздел [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="8f06a-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f06a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f06a-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="8f06a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f06a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f06a-111">*...*</span><span class="sxs-lookup"><span data-stu-id="8f06a-111">*...*</span></span> 
<span data-ttu-id="8f06a-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8f06a-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8f06a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8f06a-113">Requirements</span></span>



| <span data-ttu-id="8f06a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8f06a-114">Requirement</span></span> | <span data-ttu-id="8f06a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8f06a-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f06a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8f06a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8f06a-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f06a-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f06a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f06a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f06a-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="8f06a-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
