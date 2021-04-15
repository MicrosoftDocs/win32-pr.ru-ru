---
title: app_config Switch
description: Параметр конфигурации/АПП \_ выбирает режим настройки приложения, который позволяет использовать некоторые ключевые слова ACF в IDL-файле. С помощью этого параметра компилятора MIDL можно опустить ACF и указать интерфейс в одном IDL-файле.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config параметр MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411903"
---
# <a name="app_config-switch"></a>\_параметр конфигурации/АПП

Параметр **конфигурации \_ /АПП** выбирает режим настройки приложения, который позволяет использовать некоторые ключевые слова ACF в IDL-файле. С помощью этого параметра компилятора MIDL можно опустить ACF и указать интерфейс в одном IDL-файле.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

Microsoft RPC поддерживает использование следующих атрибутов ACF в IDL-файле:

-   Неявный \_ обработчик
-   Автоматическая \_ работа
-   Явный \_ маркер

Будущие версии Microsoft RPC могут поддерживать использование других атрибутов ACF в IDL-файле. Параметр **\_ конфигурации/АПП** представляет собой расширение Microsoft для спецификации использование-DCE и, как таковое, является взаимоисключающим с параметром [**/ОСФ**](-osf.md) .

Дополнительные сведения о параметре **\_ конфигурации/АПП** см. в разделе [файл конфигурации приложения (ACF)](application-configuration-file-acf-.md) и [файл определения интерфейса (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Примеры

**MIDL/АПП \_ config filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




