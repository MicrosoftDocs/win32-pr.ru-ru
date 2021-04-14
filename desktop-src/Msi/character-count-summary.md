---
description: Свойство "Сводка числа символов" используется только в преобразованиях.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Свойство сводки количества символов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668569"
---
# <a name="character-count-summary-property"></a><span data-ttu-id="ca035-103">Свойство сводки количества символов</span><span class="sxs-lookup"><span data-stu-id="ca035-103">Character Count Summary property</span></span>

<span data-ttu-id="ca035-104">Свойство " **Сводка числа символов** " используется только в преобразованиях.</span><span class="sxs-lookup"><span data-stu-id="ca035-104">The **Character Count Summary** property is only used in transforms.</span></span> <span data-ttu-id="ca035-105">Эта часть информационного потока сводки делится на 2 16-разрядные слова.</span><span class="sxs-lookup"><span data-stu-id="ca035-105">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="ca035-106">В верхнем слове содержатся [*Флаги проверки преобразования*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ca035-106">The upper word contains the [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="ca035-107">В нижнем слове содержатся [*флаги состояния ошибки преобразования*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ca035-107">The lower word contains the [*transform error condition flags*](t-gly.md).</span></span>

<span data-ttu-id="ca035-108">Это свойство должно иметь значение NULL в пакете установки или пакете исправлений.</span><span class="sxs-lookup"><span data-stu-id="ca035-108">This property should be Null in an installation package or patch package.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca035-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ca035-109">Requirements</span></span>



| <span data-ttu-id="ca035-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ca035-110">Requirement</span></span> | <span data-ttu-id="ca035-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ca035-111">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca035-112">Версия</span><span class="sxs-lookup"><span data-stu-id="ca035-112">Version</span></span><br/> | <span data-ttu-id="ca035-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca035-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca035-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca035-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca035-115">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca035-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca035-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca035-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca035-117">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="ca035-117">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




