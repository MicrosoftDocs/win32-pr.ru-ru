---
description: Метод Set задает значение заданного свойства звуковых параметров.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'Метод Итаудиосеттингс:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679727"
---
# <a name="itaudiosettingsset-method"></a><span data-ttu-id="161cb-103">Метод Итаудиосеттингс:: Set</span><span class="sxs-lookup"><span data-stu-id="161cb-103">ITAudioSettings::Set method</span></span>

<span data-ttu-id="161cb-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="161cb-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="161cb-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="161cb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="161cb-106">Метод **Set** задает значение заданного [**Свойства звуковых параметров**](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="161cb-106">The **Set** method sets the value of a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="161cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="161cb-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="161cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="161cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="161cb-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="161cb-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161cb-110">Член перечисления [**аудиосеттингспроперти**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="161cb-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="161cb-111">*lvalue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="161cb-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161cb-112">Требуемое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="161cb-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="161cb-113">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="161cb-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161cb-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="161cb-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="161cb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="161cb-115">Return value</span></span>

<span data-ttu-id="161cb-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="161cb-116">This method can return one of these values.</span></span>



| <span data-ttu-id="161cb-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="161cb-117">Return code</span></span>                                                                                   | <span data-ttu-id="161cb-118">Описание</span><span class="sxs-lookup"><span data-stu-id="161cb-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="161cb-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="161cb-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="161cb-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="161cb-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="161cb-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="161cb-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="161cb-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="161cb-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="161cb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="161cb-123">Requirements</span></span>



| <span data-ttu-id="161cb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="161cb-124">Requirement</span></span> | <span data-ttu-id="161cb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="161cb-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="161cb-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="161cb-126">TAPI version</span></span><br/> | <span data-ttu-id="161cb-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="161cb-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="161cb-128">Header</span><span class="sxs-lookup"><span data-stu-id="161cb-128">Header</span></span><br/>       | <dl> <span data-ttu-id="161cb-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="161cb-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="161cb-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="161cb-130">Library</span></span><br/>      | <dl> <span data-ttu-id="161cb-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="161cb-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="161cb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="161cb-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="161cb-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="161cb-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="161cb-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="161cb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="161cb-135">**итаудиосеттингс**</span><span class="sxs-lookup"><span data-stu-id="161cb-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="161cb-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="161cb-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="161cb-137">**аудиосеттингспроперти**</span><span class="sxs-lookup"><span data-stu-id="161cb-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




