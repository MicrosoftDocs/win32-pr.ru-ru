---
description: Представляет конфигурацию истории файлов пользователя, под которым создается объект Фхконфигмгр. Все операции настройки выполняются путем вызова методов интерфейса Ифхконфигмгр.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Класс Фхконфигмгр (Фхкфг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895845"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="4fe61-104">Класс Фхконфигмгр</span><span class="sxs-lookup"><span data-stu-id="4fe61-104">FhConfigMgr class</span></span>

<span data-ttu-id="4fe61-105">Представляет конфигурацию истории файлов пользователя, под которым создается объект **фхконфигмгр** .</span><span class="sxs-lookup"><span data-stu-id="4fe61-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="4fe61-106">Все операции настройки выполняются путем вызова методов интерфейса [**ифхконфигмгр**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .</span><span class="sxs-lookup"><span data-stu-id="4fe61-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="4fe61-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="4fe61-107">When to implement</span></span>

<span data-ttu-id="4fe61-108">API истории файлов реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4fe61-108">The File History API implements this class.</span></span> <span data-ttu-id="4fe61-109">Чтобы создать экземпляр этого класса, используйте функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="4fe61-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe61-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4fe61-110">Requirements</span></span>



| <span data-ttu-id="4fe61-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4fe61-111">Requirement</span></span> | <span data-ttu-id="4fe61-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4fe61-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe61-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fe61-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe61-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4fe61-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4fe61-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fe61-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe61-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4fe61-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4fe61-117">Header</span><span class="sxs-lookup"><span data-stu-id="4fe61-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe61-118"><dt>Фхкфг. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe61-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fe61-119">IDL</span><span class="sxs-lookup"><span data-stu-id="4fe61-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fe61-120"><dt>Фхкфг. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fe61-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
