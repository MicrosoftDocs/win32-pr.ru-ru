---
description: Создает дополнительный экземпляр интерфейса IEnumWiaItem2 и отправляет обратный указатель на него.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Метод IEnumWiaItem2:: Clone (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810804"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="899e9-103">Метод IEnumWiaItem2:: Clone</span><span class="sxs-lookup"><span data-stu-id="899e9-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="899e9-104">Создает дополнительный экземпляр интерфейса [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) и отправляет обратный указатель на него.</span><span class="sxs-lookup"><span data-stu-id="899e9-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="899e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="899e9-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="899e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="899e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899e9-107">*ппиенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="899e9-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="899e9-108">Тип: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="899e9-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="899e9-109">Получает адрес экземпляра интерфейса [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) , который создается **IEnumWiaItem2:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="899e9-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899e9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="899e9-110">Return value</span></span>

<span data-ttu-id="899e9-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="899e9-111">Type: **HRESULT**</span></span>

<span data-ttu-id="899e9-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="899e9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="899e9-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="899e9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="899e9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="899e9-114">Remarks</span></span>

<span data-ttu-id="899e9-115">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенум* .</span><span class="sxs-lookup"><span data-stu-id="899e9-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="899e9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="899e9-116">Requirements</span></span>



| <span data-ttu-id="899e9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="899e9-117">Requirement</span></span> | <span data-ttu-id="899e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="899e9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="899e9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="899e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="899e9-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="899e9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="899e9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="899e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="899e9-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="899e9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="899e9-123">Header</span><span class="sxs-lookup"><span data-stu-id="899e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="899e9-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="899e9-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="899e9-125">IDL</span><span class="sxs-lookup"><span data-stu-id="899e9-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="899e9-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="899e9-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
