---
description: Независимые поставщики программного обеспечения могут расширять набор известных папок в системе путем регистрации собственных папок.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Расширение известных папок с помощью пользовательских папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264421"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Расширение известных папок с помощью пользовательских папок

Независимые поставщики программного обеспечения могут расширять набор известных папок в системе путем регистрации собственных папок. После регистрации эти сторонние папки известны системе. Они обнаруживаются любым вызовом [**икновнфолдерманажер:: жетфолдеридс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Обратите внимание, что известная папка должна быть папкой на компьютере. Нельзя создать известную папку для пользователя.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Определите свою известную папку с помощью структуры [**\_ определения кновнфолдер**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .

### <a name="step-2"></a>Шаг 2.

Зарегистрируйте известную папку с помощью вызова [**икновнфолдерманажер:: регистерфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Примечания

При создании известной папки для приложения в рамках процедуры установки необходимо также включить [**икновнфолдерманажер:: унрегистерфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) в составе кода удаления.

Обратите внимание на необходимость включения папки в известную систему папок перед ее регистрацией. У вас должна быть допустимая причина повышения прав доступа к папке до такого уровня видимости системы.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Пример: известные папки](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
