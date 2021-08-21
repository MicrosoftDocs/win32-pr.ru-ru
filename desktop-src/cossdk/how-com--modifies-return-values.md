---
description: Изменение возвращаемых значений COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Изменение возвращаемых значений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba2b8a9761c7bb669982b47d94b7d522298fa6d557d197d24ea4cb5e56a0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813825"
---
# <a name="how-com-modifies-return-values"></a>Изменение возвращаемых значений COM+

COM+ никогда не изменяет возвращаемое значение **HRESULT** , которое указывает на сбой, например "e \_ непредвиденно" или "e \_ Failed". Однако если объект, использующий функциональность COM+, возвращает значение **HRESULT** , указывающее на успешное выполнение (например \_ , S OK, s \_ false или No Error), COM+ иногда преобразует значение **HRESULT** в код ошибки COM+, прежде чем возвратить вызывающему объекту.

Например, если приложение возвращает значение S \_ ОК после вызова [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), если объект является корнем транзакции, которая не может быть зафиксирована, то значение **HRESULT** преобразуется в контекст \_ E, \_ Прерванный.

Когда COM+ преобразует значение **HRESULT** , он очищает все выходные параметры метода. Возвращаемые ссылки освобождаются, а значения возвращаемых указателей объектов устанавливаются в **значение NULL**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Изоляция сбоев и политика FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Поиск источника ошибки](finding-the-source-of-an-error.md)
</dt> <dt>

[Анализ кодов ошибок](interpreting-error-codes.md)
</dt> <dt>

[Стратегии обработки ошибок в COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Устранение неполадок](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



