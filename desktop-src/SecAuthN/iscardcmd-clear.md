---
description: Метод Clear очищает буферы сообщений протокола приложения (КАТЕГОРИЯХ APDU) и ответов КАТЕГОРИЯХ APDU.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'Метод Искардкмд:: Clear (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145307"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="bbc89-103">Метод Искардкмд:: Clear</span><span class="sxs-lookup"><span data-stu-id="bbc89-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="bbc89-104">\[Метод **clear** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bbc89-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bbc89-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bbc89-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bbc89-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="bbc89-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bbc89-107">Метод **clear** очищает буферы сообщений [*протокола приложения*](../secgloss/a-gly.md) (КАТЕГОРИЯХ APDU) и [*ответов категориях APDU*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc89-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbc89-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="bbc89-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbc89-109">Parameters</span></span>

<span data-ttu-id="bbc89-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bbc89-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbc89-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbc89-111">Return value</span></span>

<span data-ttu-id="bbc89-112">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="bbc89-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bbc89-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bbc89-113">Return code</span></span>                                                                             | <span data-ttu-id="bbc89-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bbc89-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bbc89-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc89-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="bbc89-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="bbc89-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bbc89-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc89-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="bbc89-118">Неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="bbc89-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bbc89-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbc89-119">Remarks</span></span>

<span data-ttu-id="bbc89-120">Чтобы создать команду КАТЕГОРИЯХ APDU, вызовите [**буилдкмд**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bbc89-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="bbc89-121">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bbc89-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="bbc89-122">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="bbc89-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bbc89-123">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bbc89-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bbc89-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="bbc89-124">Examples</span></span>

<span data-ttu-id="bbc89-125">В следующем примере показано, как очистить буферы сообщений КАТЕГОРИЯХ APDU и Reply КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="bbc89-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="bbc89-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bbc89-126">Requirements</span></span>



| <span data-ttu-id="bbc89-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc89-127">Requirement</span></span> | <span data-ttu-id="bbc89-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc89-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc89-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbc89-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc89-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bbc89-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bbc89-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbc89-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc89-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbc89-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bbc89-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bbc89-133">End of client support</span></span><br/>    | <span data-ttu-id="bbc89-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbc89-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bbc89-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bbc89-135">End of server support</span></span><br/>    | <span data-ttu-id="bbc89-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbc89-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bbc89-137">Header</span><span class="sxs-lookup"><span data-stu-id="bbc89-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc89-138"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc89-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbc89-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bbc89-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbc89-140"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bbc89-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bbc89-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bbc89-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbc89-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbc89-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbc89-143">IID</span><span class="sxs-lookup"><span data-stu-id="bbc89-143">IID</span></span><br/>                      | <span data-ttu-id="bbc89-144">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bbc89-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bbc89-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbc89-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc89-146">**Искардкмд:: Буилдкмд**</span><span class="sxs-lookup"><span data-stu-id="bbc89-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="bbc89-147">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="bbc89-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
