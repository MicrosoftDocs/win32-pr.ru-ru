---
description: Обработчик ХРЕКОГНИЗЕР используется для создания контекста распознавателя, получения атрибутов и свойств распознавателя, а также для определения свойств пакетов, необходимых распознавателю для выполнения распознавания.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: ХРЕКОГНИЗЕР (краткий обзор. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343745"
---
# <a name="hrecognizer-handle"></a>ХРЕКОГНИЗЕР, обработчик

Обработчик **хрекогнизер** используется для создания контекста распознавателя, получения атрибутов и свойств распознавателя, а также для определения свойств пакетов, необходимых распознавателю для выполнения распознавания.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Комментарии

Следующие функции используют **хрекогнизер**.



| Функция                                                               | Описание                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**креатерекогнизер**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Создает распознаватель.<br/>                                                                   |
| [**дестройрекогнизер**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Уничтожает распознаватель.<br/>                                                                  |
| [**жетрекоаттрибутес**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Возвращает атрибуты распознавателя.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Создает контекст распознавателя.<br/>                                                           |
| [**дестройконтекст**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Уничтожает контекст распознавателя.<br/>                                                          |
| [**жеталлрекогнизерс**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Получает все Распознаватели.<br/>                                                                   |
| [**жетресултпропертилист**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Получает список свойств, которые может вернуть распознаватель для диапазона результатов.<br/>            |
| [**жетпреферредпаккетдескриптион**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Извлекает описание пакета, содержащего свойства пакета, которые использует распознаватель.<br/> |
| [**жетуникодеранжес**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Извлекает диапазоны точек Юникода, которые поддерживает распознаватель.<br/>                    |
| [**лоадкачедаттрибутес**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Загружает кэшированные атрибуты распознавателя.<br/>                                            |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | <dl> <dt>Напомню. h</dt> </dl> |



 

 




