---
title: IMsRdpClientAdvancedSettings6 Коннекттоадминистерсервер, свойство
description: Возвращает или задает значение, указывающее, должен ли элемент управления ActiveX пытаться подключиться к серверу для административных целей.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннекттоадминистерсервер
- Службы удаленных рабочих столов свойства Коннекттоадминистерсервер, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннекттоадминистерсервер
- Службы удаленных рабочих столов свойства Коннекттоадминистерсервер, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннекттоадминистерсервер
- Службы удаленных рабочих столов свойства Коннекттоадминистерсервер, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннекттоадминистерсервер
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071630"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="1017b-110">Свойство IMsRdpClientAdvancedSettings6:: Коннекттоадминистерсервер</span><span class="sxs-lookup"><span data-stu-id="1017b-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="1017b-111">Возвращает или задает значение, указывающее, должен ли элемент управления ActiveX пытаться подключиться к серверу для административных целей.</span><span class="sxs-lookup"><span data-stu-id="1017b-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="1017b-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1017b-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1017b-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1017b-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="1017b-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1017b-114">Property value</span></span>

<span data-ttu-id="1017b-115">**Вариант \_ Значение TRUE** , чтобы элемент управления ActiveX пытался подключиться к серверу для административных целей. в противном случае значение **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="1017b-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="1017b-116">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="1017b-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1017b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1017b-117">Remarks</span></span>

<span data-ttu-id="1017b-118">Чтобы использовать **коннекттоадминистерсервер**, необходимо запустить клиент Подключение К УДАЛЕННОМУ РАБОЧЕМУ столу (RDC) версии 6,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1017b-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="1017b-119">RDC версии 6,1 (6.0.6001) поддерживает протокол удаленного рабочего стола 6,1.</span><span class="sxs-lookup"><span data-stu-id="1017b-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="1017b-120">RDC 6,1 входит в состав Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1017b-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="1017b-121">**Коннекттоадминистерсервер** подключает вас к сеансу, который используется для административных целей на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="1017b-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="1017b-122">Если служба роли узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) установлена на удаленном сервере, **коннекттоадминистерсервер** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1017b-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="1017b-123">Отключает лицензирование службы удаленных рабочих столов клиентского доступа для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1017b-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="1017b-124">Отключает перенаправление часового пояса для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1017b-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="1017b-125">Отключает перенаправление подключение к удаленному рабочему столу Broker (RDCB) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1017b-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="1017b-126">Отключает перенаправление устройств самонастраивающийся для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1017b-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="1017b-127">Изменяет тему удаленного сеанса на классический класс Windows для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1017b-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="1017b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1017b-128">Requirements</span></span>



| <span data-ttu-id="1017b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1017b-129">Requirement</span></span> | <span data-ttu-id="1017b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1017b-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1017b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1017b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1017b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1017b-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1017b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1017b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1017b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1017b-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1017b-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1017b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="1017b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1017b-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1017b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1017b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1017b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1017b-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1017b-139">IID</span><span class="sxs-lookup"><span data-stu-id="1017b-139">IID</span></span><br/>                      | <span data-ttu-id="1017b-140">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="1017b-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1017b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1017b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1017b-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1017b-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1017b-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1017b-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1017b-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1017b-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





