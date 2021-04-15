---
description: Для расширяемых констант данных в виде битовых флагов поставщик поставщика услуг может определять новые значения для указанных битов.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Константы данных Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683158"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="b7969-103">Константы данных Bit-Flag</span><span class="sxs-lookup"><span data-stu-id="b7969-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="b7969-104">Для расширяемых констант данных в виде битовых флагов поставщик поставщика услуг может определять новые значения для указанных битов.</span><span class="sxs-lookup"><span data-stu-id="b7969-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="b7969-105">Так как большинство констант флагов имеют значение **DWORD**, для распространенных расширений обычно зарезервировано определенное число младших битов, а оставшиеся верхние биты доступны для расширений, зависящих от поставщика.</span><span class="sxs-lookup"><span data-stu-id="b7969-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="b7969-106">Распространенным битовым флагам назначается ноль, а расширения, зависящие от поставщика, должны быть назначены с 31-й стороны.</span><span class="sxs-lookup"><span data-stu-id="b7969-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="b7969-107">Эта схема обеспечивает максимальную гибкость при назначении битовых позиций общим расширениям, в отличие от расширений, зависящих от поставщика.</span><span class="sxs-lookup"><span data-stu-id="b7969-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="b7969-108">Предполагается, что поставщик определяет новые значения, которые являются естественными расширениями битовых флагов, определенных API.</span><span class="sxs-lookup"><span data-stu-id="b7969-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="b7969-109">Расширяемые структуры данных имеют поле размера вариабли, зарезервированное для использования в конкретных устройствах.</span><span class="sxs-lookup"><span data-stu-id="b7969-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="b7969-110">Так как поле имеет размер вариабли, поставщик услуг определяет объем информации и интерпретации поля.</span><span class="sxs-lookup"><span data-stu-id="b7969-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="b7969-111">Поставщик, определяющий поле для конкретного устройства, должен сделать эти естественные расширения исходной структуры данных, определенной API.</span><span class="sxs-lookup"><span data-stu-id="b7969-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



