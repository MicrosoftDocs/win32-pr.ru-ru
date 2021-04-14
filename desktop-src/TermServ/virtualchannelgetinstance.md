---
title: Точка входа Виртуалчаннелжетинстанце
description: Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса Ивтсплугин для всех подключаемых модулей, реализованных библиотекой DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов точки входа Виртуалчаннелжетинстанце
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415145"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="474d6-104">Точка входа Виртуалчаннелжетинстанце</span><span class="sxs-lookup"><span data-stu-id="474d6-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="474d6-105">Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для всех подключаемых модулей, РЕАЛИЗОВАНных библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="474d6-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="474d6-106">Эта функция реализуется подключаемым модулем и должна быть экспортирована по имени таким, что приложение может использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к функции.</span><span class="sxs-lookup"><span data-stu-id="474d6-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="474d6-107">Прототип для этой функции не содержится в файле общедоступного заголовка, поэтому его необходимо объявить в точности так, как показано.</span><span class="sxs-lookup"><span data-stu-id="474d6-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="474d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="474d6-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="474d6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="474d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474d6-110">*рефиид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="474d6-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474d6-111">Указывает тип возвращаемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="474d6-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="474d6-112">Это должен быть **IID \_ ивтсплугин**.</span><span class="sxs-lookup"><span data-stu-id="474d6-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="474d6-113">*пнумобжс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="474d6-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="474d6-114">Адрес переменной **ulong** , которая получает число извлеченных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="474d6-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="474d6-115">*ппобжаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="474d6-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="474d6-116">Адрес массива указателей, получающих указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="474d6-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="474d6-117">Если этот параметр имеет **значение NULL**, реализация должна поставить число подключаемых модулей, реализованных библиотекой DLL, в параметре *пнумобжс* .</span><span class="sxs-lookup"><span data-stu-id="474d6-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="474d6-118">Это позволяет вызывающему объекту выделить правильный массив размера для *ппобжаррай*.</span><span class="sxs-lookup"><span data-stu-id="474d6-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474d6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="474d6-119">Return value</span></span>

<span data-ttu-id="474d6-120">Если точка входа прошла успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="474d6-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="474d6-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="474d6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="474d6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="474d6-122">Requirements</span></span>



| <span data-ttu-id="474d6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="474d6-123">Requirement</span></span> | <span data-ttu-id="474d6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="474d6-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="474d6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="474d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="474d6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="474d6-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="474d6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="474d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="474d6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="474d6-128">Windows Server 2008</span></span><br/> |



 

