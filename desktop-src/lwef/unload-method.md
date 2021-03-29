---
title: Метод выгрузки
description: Метод выгрузки
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790585"
---
# <a name="unload-method"></a>Метод выгрузки

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Выгружает символьные данные для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Characters. Unload "*** чарактерид * * *"**

</dd> </dl>

## <a name="remarks"></a>Комментарии

Используйте этот метод, если символ больше не нужен, чтобы освободить память, используемую для хранения сведений об этом символе. При повторном доступе к символу используйте метод [**Load**](load-method.md) .

Этот метод не возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .

 

 