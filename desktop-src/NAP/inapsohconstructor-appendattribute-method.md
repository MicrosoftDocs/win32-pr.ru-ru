---
title: Метод Инапсохконструктор Аппендаттрибуте (Наппротокол. h)
description: Добавляет TLV в конец буфера SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Метод Аппендаттрибуте NAP
- Метод Аппендаттрибуте NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Аппендаттрибуте
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534094"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="eea8c-106">Метод Инапсохконструктор:: Аппендаттрибуте</span><span class="sxs-lookup"><span data-stu-id="eea8c-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="eea8c-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="eea8c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="eea8c-108">Метод **инапсохконструктор:: аппендаттрибуте** добавляет TLV в конец буфера SoH.</span><span class="sxs-lookup"><span data-stu-id="eea8c-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea8c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eea8c-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="eea8c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eea8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea8c-111">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eea8c-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea8c-112">Перечисление [**сохаттрибутетипе**](sohattributetype-enum.md) , указывающее тип атрибута нового TLV.</span><span class="sxs-lookup"><span data-stu-id="eea8c-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="eea8c-113">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eea8c-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea8c-114">Указатель на структуру [**сохаттрибутевалуе**](sohattributevalue-union.md) , содержащую значение для нового TLV.</span><span class="sxs-lookup"><span data-stu-id="eea8c-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea8c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eea8c-115">Return value</span></span>

<span data-ttu-id="eea8c-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="eea8c-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="eea8c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eea8c-117">Return code</span></span>                                                                                     | <span data-ttu-id="eea8c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="eea8c-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="eea8c-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="eea8c-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="eea8c-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="eea8c-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="eea8c-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="eea8c-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="eea8c-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="eea8c-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eea8c-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eea8c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eea8c-125">Remarks</span></span>

<span data-ttu-id="eea8c-126">Не следует добавлять TLV [**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md) с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="eea8c-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="eea8c-127">Он добавляется в качестве первого TLV путем [**инапсохконструктор:: Initialize**](inapsohconstructor-initialize-method.md) для вновь сконструированных пакетов SoH.</span><span class="sxs-lookup"><span data-stu-id="eea8c-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="eea8c-128">При добавлении атрибута, который будет использоваться системой защиты доступа к сети, он не должен быть зашифрован или изменен каким бы то ни было образом.</span><span class="sxs-lookup"><span data-stu-id="eea8c-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="eea8c-129">Если для Хеалсентити требуется проверка шифрования и целостности (Mac) частной информации, она должна быть включена только в атрибут [**сохаттрибутетипевендорспеЦифик**](sohattributetype-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="eea8c-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea8c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="eea8c-130">Requirements</span></span>



| <span data-ttu-id="eea8c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="eea8c-131">Requirement</span></span> | <span data-ttu-id="eea8c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="eea8c-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea8c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eea8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eea8c-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eea8c-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eea8c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eea8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eea8c-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eea8c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eea8c-137">Header</span><span class="sxs-lookup"><span data-stu-id="eea8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea8c-138"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="eea8c-139">IDL</span><span class="sxs-lookup"><span data-stu-id="eea8c-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eea8c-140"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="eea8c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eea8c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea8c-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea8c-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="eea8c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eea8c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea8c-144">**инапсохконструктор**</span><span class="sxs-lookup"><span data-stu-id="eea8c-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





