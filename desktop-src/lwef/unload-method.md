---
title: Метод выгрузки
description: Метод выгрузки
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474502"
---
# <a name="unload-method"></a>Метод выгрузки

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Выгружает символьные данные для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Characters. Unload "**_чарактерид_*_"_*

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте этот метод, если символ больше не нужен, чтобы освободить память, используемую для хранения сведений об этом символе. При повторном доступе к символу используйте метод [**Load**](load-method.md) .

Этот метод не возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .

 

 