---
description: Указывает, должны ли сообщения контекста отправляться в оконную процедуру окна-владельца.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Перечисление CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816832"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="0c5a6-103">\_ \_ Перечисление типов включения контекста</span><span class="sxs-lookup"><span data-stu-id="0c5a6-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="0c5a6-104">Указывает, должны ли сообщения контекста отправляться в оконную процедуру окна-владельца.</span><span class="sxs-lookup"><span data-stu-id="0c5a6-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c5a6-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0c5a6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="0c5a6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c5a6-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_включение контекста**</span><span class="sxs-lookup"><span data-stu-id="0c5a6-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c5a6-108">Необходимо включить контекст планшета, в результате чего сообщения контекста отправляются в оконную процедуру окна-владельца.</span><span class="sxs-lookup"><span data-stu-id="0c5a6-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0c5a6-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**\_Отключение контекста**</span><span class="sxs-lookup"><span data-stu-id="0c5a6-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c5a6-110">Контекст планшета должен быть отключен, предотвращая дальнейшую отправку сообщений контекста в процедуру окна или приемник событий окна-владельца.</span><span class="sxs-lookup"><span data-stu-id="0c5a6-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c5a6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0c5a6-111">Requirements</span></span>



| <span data-ttu-id="0c5a6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0c5a6-112">Requirement</span></span> | <span data-ttu-id="0c5a6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0c5a6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0c5a6-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c5a6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5a6-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0c5a6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c5a6-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c5a6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5a6-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c5a6-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="0c5a6-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c5a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5a6-119">**Метод Итаблет:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="0c5a6-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




