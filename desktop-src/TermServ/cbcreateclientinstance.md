---
title: Функция Кбкреатеклиентинстанце (Кбклиент. h)
description: Создает экземпляр клиента RPC компонента подключение к удаленному рабочему столу Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Кбкреатеклиентинстанце
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680048"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="806c7-104">Функция Кбкреатеклиентинстанце</span><span class="sxs-lookup"><span data-stu-id="806c7-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="806c7-105">Создает экземпляр клиента RPC компонента подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="806c7-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="806c7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="806c7-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="806c7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="806c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806c7-108">*Версия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="806c7-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806c7-109">Указывает версию запрашиваемого интерфейса клиента компонента подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="806c7-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="806c7-110">Это должно быть следующее значение.</span><span class="sxs-lookup"><span data-stu-id="806c7-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="806c7-111">1</span><span class="sxs-lookup"><span data-stu-id="806c7-111">1</span></span>
</dt> <dd>

<span data-ttu-id="806c7-112">Версия 1 клиента брокера подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="806c7-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="806c7-113">*ппкбклиент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="806c7-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="806c7-114">Адрес указателя интерфейса [**иконнектионброкерклиент**](iconnectionbrokerclient.md) , который получает объект клиента компонента Подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="806c7-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="806c7-115">Return value</span></span>

<span data-ttu-id="806c7-116">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="806c7-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="806c7-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="806c7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="806c7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="806c7-118">Requirements</span></span>



| <span data-ttu-id="806c7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="806c7-119">Requirement</span></span> | <span data-ttu-id="806c7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="806c7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="806c7-121">Header</span><span class="sxs-lookup"><span data-stu-id="806c7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="806c7-122"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="806c7-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="806c7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="806c7-123">Library</span></span><br/> | <dl> <span data-ttu-id="806c7-124"><dt>Кбклиент. lib</dt></span><span class="sxs-lookup"><span data-stu-id="806c7-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="806c7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="806c7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="806c7-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="806c7-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





