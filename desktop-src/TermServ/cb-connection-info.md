---
title: Структура CB_CONNECTION_INFO (Кбклиент. h)
description: Содержит сведения о входящем запросе на подключение.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO структуры службы удаленных рабочих столов
- PCB_CONNECTION_INFO службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415088"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="d57ba-105">\_ \_ Структура сведений о СОЕДИНЕНии CB</span><span class="sxs-lookup"><span data-stu-id="d57ba-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="d57ba-106">Содержит сведения о входящем запросе на подключение.</span><span class="sxs-lookup"><span data-stu-id="d57ba-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="d57ba-107">Эта структура используется с методом [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d57ba-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57ba-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d57ba-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="d57ba-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d57ba-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d57ba-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d57ba-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-111">Имя пользователя, запросившего сеанс.</span><span class="sxs-lookup"><span data-stu-id="d57ba-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-112">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="d57ba-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-113">Имя домена, членом которого является имя **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="d57ba-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-114">**инитиалпрограм**</span><span class="sxs-lookup"><span data-stu-id="d57ba-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-115">Полный путь и имя файла начальной программы, которая запускается при запуске сеанса.</span><span class="sxs-lookup"><span data-stu-id="d57ba-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="d57ba-116">Если начальная программа не должна запускаться, присвойте этому элементу пустую строку.</span><span class="sxs-lookup"><span data-stu-id="d57ba-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-117">**Ресурс**</span><span class="sxs-lookup"><span data-stu-id="d57ba-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-118">Значение перечисления [**\_ \_ типа ресурса CB**](cb-resource-type.md) , указывающее тип ресурса, к которому подключается входящее подключение.</span><span class="sxs-lookup"><span data-stu-id="d57ba-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="d57ba-119">Если элемент **PluginName** имеет **значение NULL**, этот член используется компонентом подключение к удаленному рабочему столу Broker, чтобы определить, какой подключаемый модуль следует вызвать для определения целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d57ba-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="d57ba-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-121">Имя подключаемого модуля, вызываемого для определения целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d57ba-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="d57ba-122">Если этот параметр имеет **значение NULL**, то для определения подключаемого модуля используется член **ресурса** .</span><span class="sxs-lookup"><span data-stu-id="d57ba-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-123">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="d57ba-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-124">Имя фермы, содержащей компьютеры, один из которых будет целевым компьютером, на который будет перенаправлено подключение.</span><span class="sxs-lookup"><span data-stu-id="d57ba-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-125">**дввендоринфоленгс**</span><span class="sxs-lookup"><span data-stu-id="d57ba-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-126">Этот элемент зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="d57ba-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d57ba-127">**пвендорспеЦифиЦинфо**</span><span class="sxs-lookup"><span data-stu-id="d57ba-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d57ba-128">Этот элемент зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="d57ba-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d57ba-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d57ba-129">Requirements</span></span>



| <span data-ttu-id="d57ba-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d57ba-130">Requirement</span></span> | <span data-ttu-id="d57ba-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d57ba-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d57ba-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d57ba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d57ba-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d57ba-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="d57ba-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d57ba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d57ba-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d57ba-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="d57ba-136">Header</span><span class="sxs-lookup"><span data-stu-id="d57ba-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57ba-137"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57ba-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57ba-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d57ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57ba-139">**Иконнектионброкерклиент:: Жеттаржетинфо**</span><span class="sxs-lookup"><span data-stu-id="d57ba-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





