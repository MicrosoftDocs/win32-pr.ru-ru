---
title: Метод Инапсохпроцессор-Attribute (Наппротокол. h)
description: Извлекает тип и значение атрибута с учетом расположения атрибута.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Метод OutAttribute NAP
- Метод OutAttribute NAP, интерфейс Инапсохпроцессор
- Инапсохпроцессор интерфейса NAP, метод InAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672487"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="65b44-106">Метод Инапсохпроцессор:: OutAttribute</span><span class="sxs-lookup"><span data-stu-id="65b44-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="65b44-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="65b44-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="65b44-108">Метод **инапсохпроцессор:: InAttribute** Извлекает тип и значение атрибута с учетом расположения атрибута.</span><span class="sxs-lookup"><span data-stu-id="65b44-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b44-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65b44-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="65b44-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="65b44-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b44-111">*аттрибутелокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65b44-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b44-112">Расположение (индекс) атрибута, тип и значение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="65b44-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="65b44-113">Значение *аттрибутелокатион* возвращается при предыдущем вызове метода [**Инапсохпроцессор:: финднекстаттрибуте**](inapsohprocessor-findnextattribute-method.md).</span><span class="sxs-lookup"><span data-stu-id="65b44-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="65b44-114">*тип* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65b44-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b44-115">Указатель на структуру [**сохаттрибутетипе**](sohattributetype-enum.md) , указывающую тип атрибута в *значении*.</span><span class="sxs-lookup"><span data-stu-id="65b44-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="65b44-116">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65b44-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b44-117">Указатель на указатель на структуру [**сохаттрибутевалуе**](sohattributevalue-union.md) , которая содержит значение атрибута в соответствии с определением *типа*.</span><span class="sxs-lookup"><span data-stu-id="65b44-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b44-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65b44-118">Return value</span></span>

<span data-ttu-id="65b44-119">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="65b44-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="65b44-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="65b44-120">Return code</span></span>                                                                                     | <span data-ttu-id="65b44-121">Описание</span><span class="sxs-lookup"><span data-stu-id="65b44-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="65b44-122"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="65b44-123">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="65b44-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="65b44-124"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="65b44-125">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="65b44-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="65b44-126"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="65b44-127">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65b44-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="65b44-128">Требования</span><span class="sxs-lookup"><span data-stu-id="65b44-128">Requirements</span></span>



| <span data-ttu-id="65b44-129">Требование</span><span class="sxs-lookup"><span data-stu-id="65b44-129">Requirement</span></span> | <span data-ttu-id="65b44-130">Значение</span><span class="sxs-lookup"><span data-stu-id="65b44-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b44-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65b44-131">Minimum supported client</span></span><br/> | <span data-ttu-id="65b44-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65b44-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65b44-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65b44-133">Minimum supported server</span></span><br/> | <span data-ttu-id="65b44-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65b44-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="65b44-135">Header</span><span class="sxs-lookup"><span data-stu-id="65b44-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b44-136"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="65b44-137">IDL</span><span class="sxs-lookup"><span data-stu-id="65b44-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65b44-138"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="65b44-139">DLL</span><span class="sxs-lookup"><span data-stu-id="65b44-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b44-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b44-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="65b44-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65b44-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b44-142">**инапсохпроцессор**</span><span class="sxs-lookup"><span data-stu-id="65b44-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





