---
description: Делает недействительным кэш имен пользователей с ИДЕНТИФИКАТОРом безопасности.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Дисккуотаконтрол. Инвалидатесиднамекаче, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990956"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="1374f-103">Дисккуотаконтрол. Инвалидатесиднамекаче, метод</span><span class="sxs-lookup"><span data-stu-id="1374f-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="1374f-104">Делает недействительным кэш имен пользователей с ИДЕНТИФИКАТОРом безопасности.</span><span class="sxs-lookup"><span data-stu-id="1374f-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="1374f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1374f-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="1374f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1374f-106">Parameters</span></span>

<span data-ttu-id="1374f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1374f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1374f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1374f-108">Return value</span></span>

<span data-ttu-id="1374f-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1374f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1374f-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1374f-110">Remarks</span></span>

<span data-ttu-id="1374f-111">Имена пользователей и связанные с ними идентификаторы безопасности хранятся в кэше.</span><span class="sxs-lookup"><span data-stu-id="1374f-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="1374f-112">Вы можете очистить этот кэш, вызвав **инвалидатесиднамекаче**.</span><span class="sxs-lookup"><span data-stu-id="1374f-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="1374f-113">Если впоследствии вы создадите новый объект пользователя, то эти сведения необходимо будет получить с контроллера домена, а кэш потребуется будет повторно установить.</span><span class="sxs-lookup"><span data-stu-id="1374f-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="1374f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1374f-114">Requirements</span></span>



| <span data-ttu-id="1374f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1374f-115">Requirement</span></span> | <span data-ttu-id="1374f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1374f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1374f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1374f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1374f-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1374f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1374f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1374f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1374f-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1374f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1374f-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1374f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1374f-122"><dt>Дсккуота. h</dt></span><span class="sxs-lookup"><span data-stu-id="1374f-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="1374f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1374f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1374f-124"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1374f-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1374f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1374f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1374f-126">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="1374f-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




