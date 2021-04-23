---
description: Задает поле данных в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'Искардкмд: метод ut_Data:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155106"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="9ec05-103">Искардкмд::p \_ метод данных UT</span><span class="sxs-lookup"><span data-stu-id="9ec05-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="9ec05-104">\[Метод **размещения \_ данных** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9ec05-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ec05-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9ec05-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ec05-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9ec05-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9ec05-107">Метод **размещения \_ данных** задает поле данных в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9ec05-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec05-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ec05-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="9ec05-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ec05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec05-110">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ec05-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec05-111">Указатель на объект буфера байтов (**IStream**), который должен быть скопирован в поле данных категориях APDU.</span><span class="sxs-lookup"><span data-stu-id="9ec05-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec05-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ec05-112">Return value</span></span>

<span data-ttu-id="9ec05-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9ec05-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9ec05-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ec05-114">Return code</span></span>                                                                                   | <span data-ttu-id="9ec05-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9ec05-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9ec05-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ec05-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9ec05-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="9ec05-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9ec05-119">Недопустимый параметр *pData* .</span><span class="sxs-lookup"><span data-stu-id="9ec05-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="9ec05-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9ec05-121">В *pData* передан недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="9ec05-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="9ec05-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9ec05-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9ec05-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="9ec05-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ec05-124">Remarks</span></span>

<span data-ttu-id="9ec05-125">При установке новой части данных сообщения длина поля данных вычисляется и сохраняется в параметре P3 объекта КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="9ec05-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="9ec05-126">Чтобы получить длину поля данных, вызовите [**Get \_ P3**](iscardcmd-get-p3.md).</span><span class="sxs-lookup"><span data-stu-id="9ec05-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="9ec05-127">Чтобы получить поле данных из КАТЕГОРИЯХ APDU, вызовите [**Get \_ Data**](iscardcmd-get-data.md).</span><span class="sxs-lookup"><span data-stu-id="9ec05-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ec05-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="9ec05-128">Examples</span></span>

<span data-ttu-id="9ec05-129">В следующем примере показано, как задать поле данных в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9ec05-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9ec05-130">В примере предполагается, что Пибитедата является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) , а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec05-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9ec05-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9ec05-131">Requirements</span></span>



| <span data-ttu-id="9ec05-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec05-132">Requirement</span></span> | <span data-ttu-id="9ec05-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec05-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec05-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ec05-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec05-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ec05-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ec05-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ec05-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec05-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ec05-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ec05-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9ec05-138">End of client support</span></span><br/>    | <span data-ttu-id="9ec05-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ec05-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9ec05-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9ec05-140">End of server support</span></span><br/>    | <span data-ttu-id="9ec05-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ec05-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9ec05-142">Header</span><span class="sxs-lookup"><span data-stu-id="9ec05-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec05-143"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ec05-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9ec05-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ec05-145"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ec05-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec05-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec05-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec05-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ec05-148">IID</span><span class="sxs-lookup"><span data-stu-id="9ec05-148">IID</span></span><br/>                      | <span data-ttu-id="9ec05-149">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9ec05-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9ec05-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ec05-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec05-151">**получение \_ данных**</span><span class="sxs-lookup"><span data-stu-id="9ec05-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="9ec05-152">**получение \_ P3**</span><span class="sxs-lookup"><span data-stu-id="9ec05-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="9ec05-153">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="9ec05-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
