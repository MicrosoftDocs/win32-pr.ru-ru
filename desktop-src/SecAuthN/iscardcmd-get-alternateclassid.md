---
description: Возвращает значение идентификатора альтернативного класса.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Метод Искардкмд:: get_AlternateClassId (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647613"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="2376b-103">Метод Искардкмд:: Get \_ алтернатеклассид</span><span class="sxs-lookup"><span data-stu-id="2376b-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="2376b-104">\[Метод **Get \_ алтернатеклассид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2376b-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2376b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2376b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2376b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="2376b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2376b-107">Метод **Get \_ алтернатеклассид** извлекает значение идентификатора альтернативного класса.</span><span class="sxs-lookup"><span data-stu-id="2376b-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="2376b-108">Этот метод завершится ошибкой, если альтернативный идентификатор не был задан предыдущим вызовом метода Set [**\_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="2376b-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2376b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2376b-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="2376b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2376b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2376b-111">*пбикласс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2376b-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2376b-112">Указатель на байт, содержащий альтернативное значение идентификатора класса при возврате.</span><span class="sxs-lookup"><span data-stu-id="2376b-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2376b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2376b-113">Return value</span></span>

<span data-ttu-id="2376b-114">Метод возвращает следующие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="2376b-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="2376b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2376b-115">Return code</span></span>                                                                                    | <span data-ttu-id="2376b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2376b-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2376b-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="2376b-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2376b-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="2376b-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="2376b-120">Недопустимый параметр *пбикласс* .</span><span class="sxs-lookup"><span data-stu-id="2376b-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="2376b-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="2376b-122">Альтернативный идентификатор класса не был ранее задан вызовом метода Set [**\_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="2376b-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2376b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2376b-123">Remarks</span></span>

<span data-ttu-id="2376b-124">Этот метод применяется к обмену данными с помощью [*протокола T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2376b-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="2376b-125">Дополнительные сведения см. в разделе [**Размещение \_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="2376b-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2376b-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="2376b-126">Examples</span></span>

<span data-ttu-id="2376b-127">В следующем примере показано, как получить альтернативный идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="2376b-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="2376b-128">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="2376b-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2376b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2376b-129">Requirements</span></span>



| <span data-ttu-id="2376b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2376b-130">Requirement</span></span> | <span data-ttu-id="2376b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2376b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2376b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2376b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2376b-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2376b-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2376b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2376b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2376b-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2376b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2376b-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2376b-136">End of client support</span></span><br/>    | <span data-ttu-id="2376b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2376b-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2376b-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2376b-138">End of server support</span></span><br/>    | <span data-ttu-id="2376b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2376b-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2376b-140">Header</span><span class="sxs-lookup"><span data-stu-id="2376b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2376b-141"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2376b-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2376b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="2376b-143"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2376b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2376b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2376b-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2376b-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2376b-146">IID</span><span class="sxs-lookup"><span data-stu-id="2376b-146">IID</span></span><br/>                      | <span data-ttu-id="2376b-147">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2376b-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2376b-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2376b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2376b-149">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="2376b-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="2376b-150">**разместить \_ алтернатеклассид**</span><span class="sxs-lookup"><span data-stu-id="2376b-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
