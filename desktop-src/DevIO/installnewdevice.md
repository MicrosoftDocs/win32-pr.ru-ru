---
description: Устанавливает новое устройство. Пользователю предлагается выбрать устройство.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Функция Инсталлневдевице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142211"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="10d9e-104">Функция Инсталлневдевице</span><span class="sxs-lookup"><span data-stu-id="10d9e-104">InstallNewDevice function</span></span>

<span data-ttu-id="10d9e-105">Устанавливает новое устройство.</span><span class="sxs-lookup"><span data-stu-id="10d9e-105">Installs a new device.</span></span> <span data-ttu-id="10d9e-106">Пользователю предлагается выбрать устройство.</span><span class="sxs-lookup"><span data-stu-id="10d9e-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d9e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10d9e-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="10d9e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10d9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d9e-109">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10d9e-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d9e-110">Маркер окна верхнего уровня, используемый для любого требуемого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="10d9e-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="10d9e-111">*Классгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10d9e-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d9e-112">Указатель на **идентификатор GUID** класса.</span><span class="sxs-lookup"><span data-stu-id="10d9e-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="10d9e-113">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="10d9e-113">This parameter is optional.</span></span> <span data-ttu-id="10d9e-114">Если этот параметр имеет **значение NULL**, пользователь запускается на странице Выбор обнаружения.</span><span class="sxs-lookup"><span data-stu-id="10d9e-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="10d9e-115">Если этот параметр имеет **\_ значение GUID NULL** или **GUID \_ девкласс \_ Unknown**, то пользователь запускается на странице выбора класса.</span><span class="sxs-lookup"><span data-stu-id="10d9e-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="10d9e-116">*Предзагрузка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="10d9e-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10d9e-117">Указатель на переменную, которая получает состояние перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="10d9e-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="10d9e-118">Этот параметр может быть **di \_ Нидрестарт** или **di \_ нидребут**.</span><span class="sxs-lookup"><span data-stu-id="10d9e-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d9e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10d9e-119">Return value</span></span>

<span data-ttu-id="10d9e-120">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="10d9e-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="10d9e-121">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="10d9e-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="10d9e-122">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="10d9e-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="10d9e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10d9e-123">Remarks</span></span>

<span data-ttu-id="10d9e-124">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="10d9e-124">This function has no associated import library.</span></span> <span data-ttu-id="10d9e-125">Для динамической привязки к NewDev.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="10d9e-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d9e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="10d9e-126">Requirements</span></span>



| <span data-ttu-id="10d9e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="10d9e-127">Requirement</span></span> | <span data-ttu-id="10d9e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="10d9e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10d9e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10d9e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10d9e-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="10d9e-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="10d9e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10d9e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10d9e-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10d9e-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="10d9e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="10d9e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d9e-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d9e-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d9e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10d9e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d9e-136">Функции управления устройствами</span><span class="sxs-lookup"><span data-stu-id="10d9e-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

