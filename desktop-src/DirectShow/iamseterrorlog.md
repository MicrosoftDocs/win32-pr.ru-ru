---
description: Интерфейс Иамсетеррорлог задает или получает журнал ошибок в службах редактирования DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Интерфейс Иамсетеррорлог (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651793"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="f5176-103">Интерфейс Иамсетеррорлог</span><span class="sxs-lookup"><span data-stu-id="f5176-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="f5176-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f5176-104">\[Deprecated.</span></span> <span data-ttu-id="f5176-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5176-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5176-106">`IAMSetErrorLog`Интерфейс задает или получает журнал ошибок в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="f5176-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="f5176-107">Объект временной шкалы реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f5176-107">The timeline object implements this interface.</span></span> <span data-ttu-id="f5176-108">Приложения могут использовать этот интерфейс для регистрации ошибок отрисовки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f5176-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="f5176-109">Реализуйте интерфейс [**иамеррорлог**](iamerrorlog.md) в приложении, а затем вызовите метод [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="f5176-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="f5176-110">Дополнительные сведения об использовании этого интерфейса см. в разделе [ведение журнала ошибок](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f5176-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="f5176-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="f5176-111">Members</span></span>

<span data-ttu-id="f5176-112">Интерфейс **иамсетеррорлог** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f5176-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f5176-113">**Иамсетеррорлог** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5176-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="f5176-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f5176-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5176-115">Методы</span><span class="sxs-lookup"><span data-stu-id="f5176-115">Methods</span></span>

<span data-ttu-id="f5176-116">Интерфейс **иамсетеррорлог** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f5176-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="f5176-117">Метод</span><span class="sxs-lookup"><span data-stu-id="f5176-117">Method</span></span>                                               | <span data-ttu-id="f5176-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f5176-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="f5176-119">**получить \_ журнал ошибок**</span><span class="sxs-lookup"><span data-stu-id="f5176-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="f5176-120">Извлекает текущий журнал ошибок для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="f5176-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="f5176-121">**Размещение \_ ErrorLog**</span><span class="sxs-lookup"><span data-stu-id="f5176-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="f5176-122">Указывает журнал ошибок для объекта.</span><span class="sxs-lookup"><span data-stu-id="f5176-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="f5176-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5176-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f5176-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f5176-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5176-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5176-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5176-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f5176-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5176-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f5176-127">Requirements</span></span>



| <span data-ttu-id="f5176-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f5176-128">Requirement</span></span> | <span data-ttu-id="f5176-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f5176-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5176-130">Header</span><span class="sxs-lookup"><span data-stu-id="f5176-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f5176-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5176-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5176-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5176-132">Library</span></span><br/> | <dl> <span data-ttu-id="f5176-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5176-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
