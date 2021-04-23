---
description: Эксперт должен реализовать функцию регистрации экспертов. Сетевой монитор вызывает функцию регистрации экспертов для получения сведений о эксперте.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Регистрация функции обратного вызова эксперта (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898830"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="a998e-104">Регистрация функции обратного вызова эксперта</span><span class="sxs-lookup"><span data-stu-id="a998e-104">Register Expert callback function</span></span>

<span data-ttu-id="a998e-105">Эксперт должен реализовать функцию **регистрации** экспертов.</span><span class="sxs-lookup"><span data-stu-id="a998e-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="a998e-106">Сетевой монитор вызывает функцию **регистрации** экспертов для получения сведений о эксперте.</span><span class="sxs-lookup"><span data-stu-id="a998e-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="a998e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a998e-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a998e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a998e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a998e-109">*пекспертинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a998e-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a998e-110">Указатель на структуру [**експертенуминфо**](expertenuminfo.md) , которая сетевой монитор выделяется.</span><span class="sxs-lookup"><span data-stu-id="a998e-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="a998e-111">Эксперт заполняет структуру всеми запрошенными сведениями.</span><span class="sxs-lookup"><span data-stu-id="a998e-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a998e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a998e-112">Return value</span></span>

<span data-ttu-id="a998e-113">Если функция выполнена успешно, возвращается значение **true**, а функция возвращает запрошенную информацию.</span><span class="sxs-lookup"><span data-stu-id="a998e-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="a998e-114">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="a998e-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a998e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a998e-115">Remarks</span></span>

<span data-ttu-id="a998e-116">Элемент **версии** структуры [**експертенуминфо**](expertenuminfo.md) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a998e-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a998e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a998e-117">Requirements</span></span>



| <span data-ttu-id="a998e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a998e-118">Requirement</span></span> | <span data-ttu-id="a998e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a998e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a998e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a998e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a998e-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a998e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a998e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a998e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a998e-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a998e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a998e-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a998e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a998e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a998e-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




