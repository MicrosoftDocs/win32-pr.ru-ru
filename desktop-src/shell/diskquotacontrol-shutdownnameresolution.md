---
description: Завершает работу потока разрешения имен пользователей.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Дисккуотаконтрол. Шутдовннамересолутион, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072698"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="25126-103">Дисккуотаконтрол. Шутдовннамересолутион, метод</span><span class="sxs-lookup"><span data-stu-id="25126-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="25126-104">Завершает работу потока разрешения имен пользователей.</span><span class="sxs-lookup"><span data-stu-id="25126-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="25126-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25126-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="25126-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25126-106">Parameters</span></span>

<span data-ttu-id="25126-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="25126-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25126-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25126-108">Return value</span></span>

<span data-ttu-id="25126-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="25126-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25126-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="25126-110">Remarks</span></span>

<span data-ttu-id="25126-111">Сопоставитель имен идентификаторов безопасности (SID) преобразует SID в имена пользователей в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="25126-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="25126-112">Этот поток завершается автоматически при уничтожении связанного объекта управления квотой.</span><span class="sxs-lookup"><span data-stu-id="25126-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="25126-113">Однако в некоторых случаях поток больше не нужен, но объект еще не готов к уничтожению.</span><span class="sxs-lookup"><span data-stu-id="25126-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="25126-114">Типичным примером является отсутствие дальнейшей обработки, но клиенты по-прежнему содержат ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="25126-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="25126-115">Метод **шутдовннамересолутион** позволяет прерывать поток сопоставителя и освобождать связанные ресурсы без удаления объекта управления квотой.</span><span class="sxs-lookup"><span data-stu-id="25126-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="25126-116">При завершении работы потока сопоставителя асинхронное разрешение имен немедленно останавливается.</span><span class="sxs-lookup"><span data-stu-id="25126-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="25126-117">Если впоследствии вызовы выполняются с такими методами, как [**adduser**](diskquotacontrol-adduser.md) или [**финдусер**](diskquotacontrol-finduser.md), то объект квоты может повторно создать поток сопоставителя.</span><span class="sxs-lookup"><span data-stu-id="25126-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25126-118">Требования</span><span class="sxs-lookup"><span data-stu-id="25126-118">Requirements</span></span>



| <span data-ttu-id="25126-119">Требование</span><span class="sxs-lookup"><span data-stu-id="25126-119">Requirement</span></span> | <span data-ttu-id="25126-120">Значение</span><span class="sxs-lookup"><span data-stu-id="25126-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25126-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25126-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25126-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25126-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25126-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25126-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25126-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25126-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="25126-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="25126-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25126-126"><dt>Дсккуота. h</dt></span><span class="sxs-lookup"><span data-stu-id="25126-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="25126-127">DLL</span><span class="sxs-lookup"><span data-stu-id="25126-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25126-128"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="25126-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25126-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25126-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25126-130">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="25126-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




