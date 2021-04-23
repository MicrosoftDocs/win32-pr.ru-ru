---
title: Функция Ртмдерегистерклиент (RTM. h)
description: Функция Ртмдерегистерклиент отменяет регистрацию клиента и освобождает ресурсы, связанные с клиентом.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RAS функции Ртмдерегистерклиент
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415512"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="a54c1-104">Функция Ртмдерегистерклиент</span><span class="sxs-lookup"><span data-stu-id="a54c1-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="a54c1-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a54c1-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a54c1-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="a54c1-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a54c1-107">Функция **ртмдерегистерклиент** отменяет регистрацию клиента и освобождает ресурсы, связанные с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a54c1-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a54c1-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="a54c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a54c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54c1-110">*Клиенсандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a54c1-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54c1-111">Маркер, идентифицирующий клиента для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="a54c1-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="a54c1-112">Получите этот обработчик путем вызова [**ртмрегистерклиент**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="a54c1-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a54c1-113">Return value</span></span>

<span data-ttu-id="a54c1-114">Если функция выполнена удачно, возвращается значение NO \_ Error.</span><span class="sxs-lookup"><span data-stu-id="a54c1-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="a54c1-115">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="a54c1-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="a54c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a54c1-116">Value</span></span>                                                                                                       | <span data-ttu-id="a54c1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a54c1-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="a54c1-118"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="a54c1-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="a54c1-119">Параметр *клиенсандле* не является допустимым маркером.</span><span class="sxs-lookup"><span data-stu-id="a54c1-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="a54c1-120"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="a54c1-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="a54c1-121">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a54c1-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="a54c1-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a54c1-122">Remarks</span></span>

<span data-ttu-id="a54c1-123">Эта функция удаляет все маршруты, добавленные клиентом.</span><span class="sxs-lookup"><span data-stu-id="a54c1-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="a54c1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a54c1-124">Requirements</span></span>



| <span data-ttu-id="a54c1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a54c1-125">Requirement</span></span> | <span data-ttu-id="a54c1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a54c1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a54c1-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a54c1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a54c1-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a54c1-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a54c1-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a54c1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a54c1-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a54c1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a54c1-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a54c1-131">End of server support</span></span><br/>    | <span data-ttu-id="a54c1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a54c1-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="a54c1-133">Header</span><span class="sxs-lookup"><span data-stu-id="a54c1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a54c1-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a54c1-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="a54c1-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a54c1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a54c1-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a54c1-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="a54c1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a54c1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a54c1-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a54c1-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54c1-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a54c1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54c1-140">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="a54c1-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a54c1-141">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="a54c1-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="a54c1-142">**ртмрегистерклиент**</span><span class="sxs-lookup"><span data-stu-id="a54c1-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





