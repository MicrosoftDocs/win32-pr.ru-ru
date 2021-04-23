---
description: Указывает новый альтернативный идентификатор класса в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'Искардкмд: метод ut_AlternateClassId:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650539"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="eb4dc-103">Искардкмд::p UT \_ алтернатеклассид метод</span><span class="sxs-lookup"><span data-stu-id="eb4dc-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="eb4dc-104">\[Метод **размещения \_ алтернатеклассид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eb4dc-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eb4dc-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="eb4dc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eb4dc-107">Метод **размещения \_ алтернатеклассид** указывает новый альтернативный идентификатор класса в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="eb4dc-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb4dc-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="eb4dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb4dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4dc-110">*бикласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb4dc-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4dc-111">Альтернативный идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-111">Alternate class identifier.</span></span> <span data-ttu-id="eb4dc-112">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4dc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb4dc-113">Return value</span></span>

<span data-ttu-id="eb4dc-114">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eb4dc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eb4dc-115">Return code</span></span>                                                                                  | <span data-ttu-id="eb4dc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="eb4dc-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="eb4dc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4dc-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="eb4dc-118">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="eb4dc-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="eb4dc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4dc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="eb4dc-120">Недопустимый параметр *бикласс* .</span><span class="sxs-lookup"><span data-stu-id="eb4dc-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb4dc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb4dc-121">Remarks</span></span>

<span data-ttu-id="eb4dc-122">При обмене данными с помощью [*протокола T = 0*](../secgloss/t-gly.md)дополнительные команды карточек могут автоматически создаваться категориях APDU и отправляться в блок данных протокола передачи (тпду).</span><span class="sxs-lookup"><span data-stu-id="eb4dc-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="eb4dc-123">Дополнительные команды обычно используют тот же идентификатор класса, что и исходная команда. Указание нового идентификатора класса с помощью этого метода позволяет автоматически создаваемым командам использовать новый идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="eb4dc-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="eb4dc-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb4dc-124">Examples</span></span>

<span data-ttu-id="eb4dc-125">В следующем примере показано, как задать новый альтернативный идентификатор класса в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="eb4dc-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="eb4dc-126">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="eb4dc-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="eb4dc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="eb4dc-127">Requirements</span></span>



| <span data-ttu-id="eb4dc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="eb4dc-128">Requirement</span></span> | <span data-ttu-id="eb4dc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="eb4dc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4dc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb4dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4dc-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eb4dc-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eb4dc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb4dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4dc-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb4dc-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb4dc-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="eb4dc-134">End of client support</span></span><br/>    | <span data-ttu-id="eb4dc-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb4dc-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eb4dc-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="eb4dc-136">End of server support</span></span><br/>    | <span data-ttu-id="eb4dc-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb4dc-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eb4dc-138">Header</span><span class="sxs-lookup"><span data-stu-id="eb4dc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb4dc-139"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4dc-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb4dc-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eb4dc-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb4dc-141"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb4dc-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb4dc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="eb4dc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb4dc-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4dc-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb4dc-144">IID</span><span class="sxs-lookup"><span data-stu-id="eb4dc-144">IID</span></span><br/>                      | <span data-ttu-id="eb4dc-145">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="eb4dc-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="eb4dc-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb4dc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4dc-147">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="eb4dc-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="eb4dc-148">**получить \_ алтернатеклассид**</span><span class="sxs-lookup"><span data-stu-id="eb4dc-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
