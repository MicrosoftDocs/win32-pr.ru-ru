---
description: Создает моникер, представляющий аппаратный компонент и связанный с ним обработчик событий. Функция автозапуска использует эту функцию, чтобы разрешить приложениям использовать события автозапуска.
title: Функция Креатехардваривентмоникер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984328"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="abb95-104">Функция Креатехардваривентмоникер</span><span class="sxs-lookup"><span data-stu-id="abb95-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="abb95-105">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="abb95-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="abb95-106">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="abb95-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="abb95-107">Создает моникер, представляющий аппаратный компонент и связанный с ним обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="abb95-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="abb95-108">Функция автозапуска использует эту функцию, чтобы разрешить приложениям использовать события автозапуска.</span><span class="sxs-lookup"><span data-stu-id="abb95-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb95-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abb95-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="abb95-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="abb95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb95-111">*идентификатор CLSID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abb95-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb95-112">Тип: **рефклсид**</span><span class="sxs-lookup"><span data-stu-id="abb95-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="abb95-113">Идентификатор класса, к которому привязывается моникер.</span><span class="sxs-lookup"><span data-stu-id="abb95-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="abb95-114">*псзевенсандлер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abb95-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb95-115">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="abb95-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="abb95-116">Имя обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="abb95-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="abb95-117">*ппмоникер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abb95-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abb95-118">Тип: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="abb95-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="abb95-119">Адрес переменной указателя, получающей указатель интерфейса [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="abb95-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb95-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abb95-120">Return value</span></span>

<span data-ttu-id="abb95-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="abb95-121">Type: **HRESULT**</span></span>

<span data-ttu-id="abb95-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb95-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="abb95-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="abb95-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="abb95-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="abb95-124">Remarks</span></span>

<span data-ttu-id="abb95-125">Используйте **креатехардваривентмоникер** при регистрации работающих приложений, чтобы эти приложения имели доступ к событиям автозапуска.</span><span class="sxs-lookup"><span data-stu-id="abb95-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="abb95-126">Чтобы использовать события автозапуска в выполняющихся приложениях, необходимо сначала создать новый компонент, реализующий интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="abb95-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="abb95-127">Инициализируйте этот интерфейс со значением Иниткмдлине из записи конкретного обработчика в разделе **обработчиков** , так как автозапуск не вызывает метод [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="abb95-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="abb95-128">Необходимо вызвать **креатехардваривентмоникер** , чтобы получить моникер, представляющий компонент и его обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="abb95-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="abb95-129">Затем используйте значение, возвращенное в параметре *ппмоникер* , для регистрации компонента в запущенной таблице объектов (ROT), как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="abb95-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="abb95-130">Обратите внимание, что **креатехардваривентмоникер** не определен в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="abb95-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="abb95-131">Чтобы использовать его в коде, необходимо получить обработчик для файла Shsvcs.dll с помощью вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="abb95-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="abb95-132">Затем этот маркер используется в вызове [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения экземпляра функции **креатехардваривентмоникер** .</span><span class="sxs-lookup"><span data-stu-id="abb95-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="abb95-133">Для вызова [**ируннингобжекттабле:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) необходимо ввести в реестр следующие сведения о **AppID** .</span><span class="sxs-lookup"><span data-stu-id="abb95-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="abb95-134">Требования</span><span class="sxs-lookup"><span data-stu-id="abb95-134">Requirements</span></span>



| <span data-ttu-id="abb95-135">Требование</span><span class="sxs-lookup"><span data-stu-id="abb95-135">Requirement</span></span> | <span data-ttu-id="abb95-136">Значение</span><span class="sxs-lookup"><span data-stu-id="abb95-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abb95-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abb95-137">Minimum supported client</span></span><br/> | <span data-ttu-id="abb95-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="abb95-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="abb95-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abb95-139">Minimum supported server</span></span><br/> | <span data-ttu-id="abb95-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abb95-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abb95-141">Header</span><span class="sxs-lookup"><span data-stu-id="abb95-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb95-142"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="abb95-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="abb95-143">DLL</span><span class="sxs-lookup"><span data-stu-id="abb95-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abb95-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abb95-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
