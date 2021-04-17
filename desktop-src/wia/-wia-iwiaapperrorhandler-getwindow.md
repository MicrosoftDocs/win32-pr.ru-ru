---
description: Получает обработчик для диалогового окна, отображающего сообщения об ошибках, и предоставляет одну или несколько кнопок для продолжения, отмены или прерывания работы приложения.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: Метод Ивиаапперрорхандлер::-Window (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711963"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="1e5cd-103">Метод Ивиаапперрорхандлер:: onwindow</span><span class="sxs-lookup"><span data-stu-id="1e5cd-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="1e5cd-104">Получает обработчик для диалогового окна, отображающего сообщения об ошибках, и предоставляет одну или несколько кнопок для продолжения, отмены или прерывания работы приложения.</span><span class="sxs-lookup"><span data-stu-id="1e5cd-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e5cd-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="1e5cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e5cd-107">*ФВНД* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e5cd-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5cd-108">Тип: \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="1e5cd-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="1e5cd-109">HWND, используемый обработчиком ошибок приложения, обработчиком ошибок драйвера и обработчиком ошибок по умолчанию для диалоговых окон сообщений об устройствах (ошибки и информационные сообщения).</span><span class="sxs-lookup"><span data-stu-id="1e5cd-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="1e5cd-110">В качестве выходного значения может быть задано значение _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="1e5cd-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e5cd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e5cd-111">Return value</span></span>

<span data-ttu-id="1e5cd-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e5cd-112">Type: **HRESULT**</span></span>

<span data-ttu-id="1e5cd-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e5cd-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e5cd-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e5cd-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e5cd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e5cd-115">Remarks</span></span>

<span data-ttu-id="1e5cd-116">*ФВНД* указывает на окно, передаваемое в [**Репортстатус**](-wia-iwiaerrorhandler-reportstatus.md) с помощью прокси-сервера получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1e5cd-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="1e5cd-117">Это окно должно оставаться действительным на время пересылки данных.</span><span class="sxs-lookup"><span data-stu-id="1e5cd-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5cd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1e5cd-118">Requirements</span></span>



| <span data-ttu-id="1e5cd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1e5cd-119">Requirement</span></span> | <span data-ttu-id="1e5cd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1e5cd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5cd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e5cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5cd-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e5cd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e5cd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e5cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5cd-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e5cd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1e5cd-125">Header</span><span class="sxs-lookup"><span data-stu-id="1e5cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e5cd-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cd-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="1e5cd-127">IDL</span><span class="sxs-lookup"><span data-stu-id="1e5cd-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e5cd-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cd-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="1e5cd-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e5cd-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e5cd-130"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cd-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




