---
title: Метод Инапсохпроцессор Финднекстаттрибуте (Наппротокол. h)
description: Находит расположение (индекс) следующего атрибута типа, указанного параметром Сохаттрибутетипе.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Метод Финднекстаттрибуте NAP
- Метод Финднекстаттрибуте NAP, интерфейс Инапсохпроцессор
- Инапсохпроцессор интерфейса NAP, метод Финднекстаттрибуте
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801318"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="12b25-106">Метод Инапсохпроцессор:: Финднекстаттрибуте</span><span class="sxs-lookup"><span data-stu-id="12b25-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="12b25-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="12b25-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="12b25-108">Метод **инапсохпроцессор:: финднекстаттрибуте** находит расположение (индекс) следующего атрибута типа, указанного в *сохаттрибутетипе*.</span><span class="sxs-lookup"><span data-stu-id="12b25-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b25-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12b25-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="12b25-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="12b25-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b25-111">*фромлокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12b25-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b25-112">Начальное расположение (индекс) в пакете состояния работоспособности (SoH) для начала поиска атрибутов.</span><span class="sxs-lookup"><span data-stu-id="12b25-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="12b25-113">Это значение должно находиться в диапазоне от 0 до (**нуматтриб** -1), где **нуматтриб** извлекается с помощью [**инапсохпроцессор:: жетнумберофаттрибутес**](inapsohprocessor-getnumberofattributes-method.md).</span><span class="sxs-lookup"><span data-stu-id="12b25-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="12b25-114">Пакет SoH использует индексы атрибутов на основе 0.</span><span class="sxs-lookup"><span data-stu-id="12b25-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="12b25-115">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12b25-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b25-116">Структура [**сохаттрибутетипе**](sohattributetype-enum.md) , содержащая тип атрибута для размещения.</span><span class="sxs-lookup"><span data-stu-id="12b25-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="12b25-117">*аттрибутелокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="12b25-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12b25-118">Указатель, содержащий расположение (индекс) в пакете SoH первого атрибута типа *сохаттрибутетипе* из индекса *фромлокатион*.</span><span class="sxs-lookup"><span data-stu-id="12b25-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b25-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12b25-119">Return value</span></span>

<span data-ttu-id="12b25-120">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="12b25-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="12b25-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="12b25-121">Return code</span></span>                                                                                            | <span data-ttu-id="12b25-122">Описание</span><span class="sxs-lookup"><span data-stu-id="12b25-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="12b25-123"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="12b25-124">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="12b25-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="12b25-125"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="12b25-126">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="12b25-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="12b25-127"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="12b25-128">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12b25-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="12b25-129"><dt>**\_файл ошибок \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="12b25-130">Атрибут не найден.</span><span class="sxs-lookup"><span data-stu-id="12b25-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="12b25-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12b25-131">Remarks</span></span>

<span data-ttu-id="12b25-132">Метод **финднекстаттрибуте** ищет атрибуты типа *сохаттрибутетипе* из индекса, заданного параметром *фромлокатион* , и выше, пока не будет найдено соответствие.</span><span class="sxs-lookup"><span data-stu-id="12b25-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="12b25-133">Если совпадений не найдено, **возвращается \_ файл ошибки \_ не \_ найден** .</span><span class="sxs-lookup"><span data-stu-id="12b25-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="12b25-134">Требования</span><span class="sxs-lookup"><span data-stu-id="12b25-134">Requirements</span></span>



| <span data-ttu-id="12b25-135">Требование</span><span class="sxs-lookup"><span data-stu-id="12b25-135">Requirement</span></span> | <span data-ttu-id="12b25-136">Значение</span><span class="sxs-lookup"><span data-stu-id="12b25-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="12b25-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12b25-137">Minimum supported client</span></span><br/> | <span data-ttu-id="12b25-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12b25-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="12b25-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12b25-139">Minimum supported server</span></span><br/> | <span data-ttu-id="12b25-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12b25-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="12b25-141">Header</span><span class="sxs-lookup"><span data-stu-id="12b25-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="12b25-142"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="12b25-143">IDL</span><span class="sxs-lookup"><span data-stu-id="12b25-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12b25-144"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="12b25-145">DLL</span><span class="sxs-lookup"><span data-stu-id="12b25-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12b25-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12b25-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="12b25-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12b25-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b25-148">**инапсохпроцессор**</span><span class="sxs-lookup"><span data-stu-id="12b25-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





