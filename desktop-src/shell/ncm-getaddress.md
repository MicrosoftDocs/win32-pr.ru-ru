---
description: Указывает, соответствует ли сетевой адрес указанному типу и формату.
title: Сообщение NCM_GETADDRESS (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984600"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="c5ae3-103">\_Сообщение НКМ</span><span class="sxs-lookup"><span data-stu-id="c5ae3-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="c5ae3-104">Указывает, соответствует ли сетевой адрес указанному типу и формату.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="c5ae3-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5ae3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ae3-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5ae3-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5ae3-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5ae3-108">*ПС* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c5ae3-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="c5ae3-109">Указатель на структуру <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> для получения сведений об сетевом адресе в проанализированной форме, если в элементе управления, указанном с помощью *HWND* , проверяются формат адреса и тип.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="c5ae3-110">Вызывающее приложение отвечает за выделение памяти для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ae3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5ae3-111">Return value</span></span>

<span data-ttu-id="c5ae3-112">Возвращает одно из следующих значений типа **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="c5ae3-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c5ae3-113">Return code</span></span>                                                                                                | <span data-ttu-id="c5ae3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c5ae3-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5ae3-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="c5ae3-116">Вызывающему приложению не удалось выделить структуру [**\_ адресов NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .</span><span class="sxs-lookup"><span data-stu-id="c5ae3-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="c5ae3-117"><dt>**Ошибка \_ недостаточного \_ буфера**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="c5ae3-118">Выходной буфер слишком мал для хранения проанализированного сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="c5ae3-119"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="c5ae3-120">Строка сетевого адреса не указана ни одного типа.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c5ae3-121"><dt>**Ошибка при \_ успешном выполнении**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="c5ae3-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c5ae3-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="c5ae3-124">Отсутствует адрес в элементе управления сетевыми адресами для проверки.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="c5ae3-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5ae3-125">Remarks</span></span>

<span data-ttu-id="c5ae3-126">Используйте сообщение **НКМ- \_ Address** для проверки сетевого адреса в элементе управления "сетевой адрес" по предустановленной маске типа сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="c5ae3-127">Чтобы создать экземпляр, используйте класс **мсктлс \_ нетаддресс** , определенный в шеллапи. h.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="c5ae3-128">Вызовите [**инитнетворкаддрессконтрол**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) во время выполнения перед отправкой этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="c5ae3-129">Будет инициализирована библиотека общих элементов управления, содержащая элемент управления "сетевой адрес".</span><span class="sxs-lookup"><span data-stu-id="c5ae3-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="c5ae3-130">Это сообщение получает строку сетевого адреса из элемента управления сетевыми адресами, анализирует строку и проверяет, соответствует ли строка маске типа сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="c5ae3-131">Если строка соответствует маске, сообщение возвращает значение S \_ OK и возвращает строку из проанализированной формы в вызывающее приложение (включая номер порта, длину префикса и другие сведения об адресе), используя структуру [**\_ адресов NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) , на которую указывает *ПС*.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="c5ae3-132">Это сообщение возвращает E \_ INVALIDARG, если вызывающему приложению не удается выделить структуру, на которую указывает *ПС*.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="c5ae3-133">Анализируются представления IP-адресов версий 4 и 6 (v4/V6) для служб и сетей, а также именованные адреса Интернета и службы с использованием DNS-формата.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="c5ae3-134">Если строка сетевого адреса представляет имя узла (DNS) или службу, то значение, возвращаемое членом **PrefixLength** в [**\_ адресе NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) , равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c5ae3-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="c5ae3-135">Задайте маску типа сетевого адреса с помощью сообщения [**НКМ \_ сеталловтипе**](ncm-setallowtype.md) перед отправкой макроса **НКМ \_** .</span><span class="sxs-lookup"><span data-stu-id="c5ae3-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ae3-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ae3-136">Requirements</span></span>



| <span data-ttu-id="c5ae3-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ae3-137">Requirement</span></span> | <span data-ttu-id="c5ae3-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ae3-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ae3-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5ae3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ae3-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5ae3-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5ae3-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5ae3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ae3-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5ae3-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5ae3-143">Header</span><span class="sxs-lookup"><span data-stu-id="c5ae3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ae3-144"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ae3-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ae3-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ae3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ae3-146">**НКМ \_ жеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="c5ae3-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="c5ae3-147">**Нетаддр \_**</span><span class="sxs-lookup"><span data-stu-id="c5ae3-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




