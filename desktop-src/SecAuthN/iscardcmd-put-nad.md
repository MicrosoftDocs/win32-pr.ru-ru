---
description: Указывает адрес узла (NAD) для использования с интерфейсом Искардкмд.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'Искардкмд: метод ut_Nad:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898033"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="7ea5e-103">Искардкмд::p \_ метод UT NAD</span><span class="sxs-lookup"><span data-stu-id="7ea5e-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="7ea5e-104">\[Метод **размещения \_ NAD** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ea5e-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7ea5e-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7ea5e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7ea5e-107">Метод **размещения \_ NAD** указывает адрес узла (NAD) для использования с интерфейсом [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea5e-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="7ea5e-108">Это относится только к обмену данными по [*протоколу T = 1*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea5e-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="7ea5e-109">По умолчанию объект [**искардкмд**](iscardcmd.md) использует значение NAD, равное нулю.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea5e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ea5e-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="7ea5e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea5e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea5e-112">*бнад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ea5e-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea5e-113">Байт, представляющий используемую NAD.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea5e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ea5e-114">Return value</span></span>

<span data-ttu-id="7ea5e-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7ea5e-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7ea5e-116">Return code</span></span>                                                                                  | <span data-ttu-id="7ea5e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7ea5e-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7ea5e-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7ea5e-119">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7ea5e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7ea5e-121">Недопустимый параметр *бнад* .</span><span class="sxs-lookup"><span data-stu-id="7ea5e-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="7ea5e-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ea5e-122">Remarks</span></span>

<span data-ttu-id="7ea5e-123">Этот метод следует вызывать только в том случае, если для NAD необходимо использовать значение, отличное от нуля.</span><span class="sxs-lookup"><span data-stu-id="7ea5e-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="7ea5e-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ea5e-124">Examples</span></span>

<span data-ttu-id="7ea5e-125">В следующем примере показано, как указать адрес узла для использования с интерфейсом [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea5e-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="7ea5e-126">В примере предполагается, что Бинадвалуе является переменной типа **Byte** , которой ранее было присвоено значение, а пискардкмд является допустимым указателем на экземпляр интерфейса **искардкмд** .</span><span class="sxs-lookup"><span data-stu-id="7ea5e-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7ea5e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7ea5e-127">Requirements</span></span>



| <span data-ttu-id="7ea5e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7ea5e-128">Requirement</span></span> | <span data-ttu-id="7ea5e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7ea5e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea5e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ea5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea5e-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7ea5e-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7ea5e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ea5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea5e-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ea5e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ea5e-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7ea5e-134">End of client support</span></span><br/>    | <span data-ttu-id="7ea5e-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ea5e-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7ea5e-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7ea5e-136">End of server support</span></span><br/>    | <span data-ttu-id="7ea5e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ea5e-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7ea5e-138">Header</span><span class="sxs-lookup"><span data-stu-id="7ea5e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ea5e-139"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5e-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ea5e-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7ea5e-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ea5e-141"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5e-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ea5e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ea5e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ea5e-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5e-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ea5e-144">IID</span><span class="sxs-lookup"><span data-stu-id="7ea5e-144">IID</span></span><br/>                      | <span data-ttu-id="7ea5e-145">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7ea5e-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7ea5e-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ea5e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea5e-147">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="7ea5e-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
