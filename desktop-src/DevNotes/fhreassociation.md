---
description: Представляет функцию повторной связи с журналом файлов, которая позволяет пользователю восстановить связь с целевым объектом резервного копирования, который использовался тем же пользователем в прошлом. Повторное связывание выполняется путем вызова методов интерфейса ИфхреассоЦиатион.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Класс ФхреассоЦиатион (Фхкфг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655849"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="1ce4d-104">Класс ФхреассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="1ce4d-104">FhReassociation class</span></span>

<span data-ttu-id="1ce4d-105">Представляет функцию повторной связи с журналом файлов, которая позволяет пользователю восстановить связь с целевым объектом резервного копирования, который использовался тем же пользователем в прошлом.</span><span class="sxs-lookup"><span data-stu-id="1ce4d-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="1ce4d-106">Повторное связывание выполняется путем вызова методов интерфейса [**ифхреассоЦиатион**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .</span><span class="sxs-lookup"><span data-stu-id="1ce4d-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1ce4d-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="1ce4d-107">When to implement</span></span>

<span data-ttu-id="1ce4d-108">API истории файлов реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1ce4d-108">The File History API implements this class.</span></span> <span data-ttu-id="1ce4d-109">Чтобы создать экземпляр этого класса, используйте функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="1ce4d-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce4d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1ce4d-110">Requirements</span></span>



| <span data-ttu-id="1ce4d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1ce4d-111">Requirement</span></span> | <span data-ttu-id="1ce4d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1ce4d-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce4d-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ce4d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce4d-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ce4d-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1ce4d-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ce4d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce4d-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ce4d-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ce4d-117">Header</span><span class="sxs-lookup"><span data-stu-id="1ce4d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce4d-118"><dt>Фхкфг. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce4d-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ce4d-119">IDL</span><span class="sxs-lookup"><span data-stu-id="1ce4d-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ce4d-120"><dt>Фхкфг. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ce4d-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
