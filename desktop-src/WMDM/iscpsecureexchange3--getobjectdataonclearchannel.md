---
title: Метод Жетобжектдатаонклеарчаннел
description: Метод Жетобжектдатаонклеарчаннел передает блок данных объекта на открытый канал обратно в Windows Media диспетчер устройств.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Метод Жетобжектдатаонклеарчаннел Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694424"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="afaec-104">Метод Жетобжектдатаонклеарчаннел</span><span class="sxs-lookup"><span data-stu-id="afaec-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="afaec-105">Метод **жетобжектдатаонклеарчаннел** передает блок данных объекта на открытый канал обратно в Windows Media Диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="afaec-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="afaec-106">Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются.</span><span class="sxs-lookup"><span data-stu-id="afaec-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="afaec-107">Поэтому этот метод является более эффективным.</span><span class="sxs-lookup"><span data-stu-id="afaec-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="afaec-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afaec-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="afaec-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="afaec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afaec-110">*пдевице*</span><span class="sxs-lookup"><span data-stu-id="afaec-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="afaec-111">Указатель на объект устройства.</span><span class="sxs-lookup"><span data-stu-id="afaec-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="afaec-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="afaec-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="afaec-113">Указатель на буфер для приема данных.</span><span class="sxs-lookup"><span data-stu-id="afaec-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="afaec-114">*пдвсизе*</span><span class="sxs-lookup"><span data-stu-id="afaec-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="afaec-115">Указатель на **DWORD** , содержащий размер перемещения.</span><span class="sxs-lookup"><span data-stu-id="afaec-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afaec-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afaec-116">Return value</span></span>

<span data-ttu-id="afaec-117">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="afaec-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="afaec-118">Если метод завершается с ошибкой, возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afaec-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="afaec-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="afaec-119">Return code</span></span>                                                                                                | <span data-ttu-id="afaec-120">Описание</span><span class="sxs-lookup"><span data-stu-id="afaec-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afaec-121"><dt>**\_Проверка вмдм \_ E \_ Mac \_ не пройдена**</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="afaec-122">Недопустимый код проверки подлинности сообщения.</span><span class="sxs-lookup"><span data-stu-id="afaec-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="afaec-123"><dt>**ВМДМ \_ E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="afaec-124">Вызывающий объект не имеет прав, необходимых для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="afaec-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="afaec-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="afaec-126">Сбой метода.</span><span class="sxs-lookup"><span data-stu-id="afaec-126">The method failed.</span></span> <span data-ttu-id="afaec-127">Прекращение взаимодействия с поставщиком содержимого.</span><span class="sxs-lookup"><span data-stu-id="afaec-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="afaec-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="afaec-129">Параметр является недопустимым указателем или **пустым** .</span><span class="sxs-lookup"><span data-stu-id="afaec-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="afaec-130"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="afaec-131">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="afaec-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="afaec-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afaec-132">Remarks</span></span>

<span data-ttu-id="afaec-133">Для передачи данных Windows Media диспетчер устройств вызывает метод [трансферконтаинердатаонклеарчаннел](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) для получения данных контейнера.</span><span class="sxs-lookup"><span data-stu-id="afaec-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="afaec-134">Затем вызывается **жетобжектдатаонклеарчаннел** для передачи блоков данных объекта от поставщика содержимого в Диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afaec-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="afaec-135">Если \_ параметр S ОК возвращается с *пдвсизе* , для которого установлено значение 0, Windows Media Диспетчер устройств не запрашивает никаких дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="afaec-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="afaec-136">Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются.</span><span class="sxs-lookup"><span data-stu-id="afaec-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="afaec-137">Поэтому этот метод является более эффективным.</span><span class="sxs-lookup"><span data-stu-id="afaec-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="afaec-138">Требования</span><span class="sxs-lookup"><span data-stu-id="afaec-138">Requirements</span></span>



| <span data-ttu-id="afaec-139">Требование</span><span class="sxs-lookup"><span data-stu-id="afaec-139">Requirement</span></span> | <span data-ttu-id="afaec-140">Значение</span><span class="sxs-lookup"><span data-stu-id="afaec-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afaec-141">Header</span><span class="sxs-lookup"><span data-stu-id="afaec-141">Header</span></span><br/>  | <dl> <span data-ttu-id="afaec-142"><dt>ВМСКП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="afaec-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="afaec-143">Library</span></span><br/> | <dl> <span data-ttu-id="afaec-144"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afaec-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afaec-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afaec-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afaec-146">**Искпсекуриксчанже:: ObjectData**</span><span class="sxs-lookup"><span data-stu-id="afaec-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="afaec-147">**Интерфейс ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="afaec-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





