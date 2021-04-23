---
description: Интерфейс Иамеррорлог предоставляет метод обратного вызова для ведения журнала ошибок в службах редактирования DirectShow (DES). DES не реализует этот интерфейс.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Интерфейс Иамеррорлог (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675302"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="2f4c4-103">Интерфейс Иамеррорлог</span><span class="sxs-lookup"><span data-stu-id="2f4c4-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="2f4c4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-104">\[Deprecated.</span></span> <span data-ttu-id="2f4c4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f4c4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2f4c4-106">`IAMErrorLog`Интерфейс предоставляет метод обратного вызова для ведения журнала ошибок в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="2f4c4-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="2f4c4-107">DES не реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-107">DES does not implement this interface.</span></span> <span data-ttu-id="2f4c4-108">Чтобы выполнить ведение журнала ошибок, реализуйте этот интерфейс в приложении и вызовите [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="2f4c4-109">Если при подготовке проекта к просмотру возникает ошибка, то DES вызывает метод [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) , реализованный приложением.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="2f4c4-110">DES регистрирует ошибки только при отрисовке проекта с помощью интерфейса [**ирендеренгине**](irenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4c4-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="2f4c4-111">Например, если вы сохраняете проект в виде графа фильтра DirectShow (формат ГРФ) и воспроизводите файл графа, ведение журнала ошибок отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="2f4c4-112">Дополнительные сведения об использовании этого интерфейса см. в разделе [ведение журнала ошибок](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2f4c4-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="2f4c4-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="2f4c4-113">Members</span></span>

<span data-ttu-id="2f4c4-114">Интерфейс **иамеррорлог** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f4c4-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f4c4-115">**Иамеррорлог** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2f4c4-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="2f4c4-116">Методы</span><span class="sxs-lookup"><span data-stu-id="2f4c4-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f4c4-117">Методы</span><span class="sxs-lookup"><span data-stu-id="2f4c4-117">Methods</span></span>

<span data-ttu-id="2f4c4-118">Интерфейс **иамеррорлог** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="2f4c4-119">Метод</span><span class="sxs-lookup"><span data-stu-id="2f4c4-119">Method</span></span>                                   | <span data-ttu-id="2f4c4-120">Описание</span><span class="sxs-lookup"><span data-stu-id="2f4c4-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="2f4c4-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="2f4c4-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="2f4c4-122">Заносит в журнал ошибку.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f4c4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f4c4-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f4c4-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f4c4-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f4c4-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2f4c4-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2f4c4-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f4c4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2f4c4-127">Requirements</span></span>



| <span data-ttu-id="2f4c4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2f4c4-128">Requirement</span></span> | <span data-ttu-id="2f4c4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4c4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4c4-130">Header</span><span class="sxs-lookup"><span data-stu-id="2f4c4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2f4c4-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f4c4-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2f4c4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f4c4-132">Library</span></span><br/> | <dl> <span data-ttu-id="2f4c4-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f4c4-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
