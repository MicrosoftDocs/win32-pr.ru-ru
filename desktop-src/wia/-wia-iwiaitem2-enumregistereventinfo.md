---
description: 'Метод IWiaItem2:: Енумрегистеревентинфо создает перечислитель, который можно использовать для получения сведений о событиях, для которых зарегистрировано приложение.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Метод IWiaItem2:: Енумрегистеревентинфо (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145418"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="9ac23-103">Метод IWiaItem2:: Енумрегистеревентинфо</span><span class="sxs-lookup"><span data-stu-id="9ac23-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="9ac23-104">Метод **IWiaItem2:: енумрегистеревентинфо** создает перечислитель, который можно использовать для получения сведений о событиях, для которых зарегистрировано приложение.</span><span class="sxs-lookup"><span data-stu-id="9ac23-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ac23-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9ac23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ac23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac23-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="9ac23-108">Type: **LONG**</span></span>

<span data-ttu-id="9ac23-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9ac23-109">Not used.</span></span> <span data-ttu-id="9ac23-110">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9ac23-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-111">*певентгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-112">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="9ac23-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="9ac23-113">Указатель на идентификатор, указывающий событие оборудования, для которого требуется получить сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="9ac23-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-115">Тип: **[ **иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="9ac23-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="9ac23-116">Адрес указателя на интерфейс [**\_ \_ Caps иенумвиа dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="9ac23-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac23-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ac23-117">Return value</span></span>

<span data-ttu-id="9ac23-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ac23-118">Type: **HRESULT**</span></span>

<span data-ttu-id="9ac23-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9ac23-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ac23-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ac23-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac23-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ac23-121">Remarks</span></span>

<span data-ttu-id="9ac23-122">Приложение вызывает этот метод для создания объекта перечислителя для сведений о событии.</span><span class="sxs-lookup"><span data-stu-id="9ac23-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="9ac23-123">**IWiaItem2:: енумрегистеревентинфо** сохраняет адрес интерфейса [**\_ \_ Caps иенумвиа dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) объекта перечислителя в параметре *ппиенум* .</span><span class="sxs-lookup"><span data-stu-id="9ac23-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="9ac23-124">Затем программа использует указатель интерфейса для перечисления свойств события, для которого оно зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="9ac23-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="9ac23-125">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ппиенум* .</span><span class="sxs-lookup"><span data-stu-id="9ac23-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac23-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9ac23-126">Requirements</span></span>



| <span data-ttu-id="9ac23-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9ac23-127">Requirement</span></span> | <span data-ttu-id="9ac23-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9ac23-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ac23-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ac23-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac23-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ac23-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ac23-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac23-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ac23-133">Header</span><span class="sxs-lookup"><span data-stu-id="9ac23-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ac23-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
