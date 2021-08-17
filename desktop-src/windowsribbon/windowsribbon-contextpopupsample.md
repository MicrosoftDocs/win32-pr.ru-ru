---
title: Пример Контекстпопуп
description: в этом примере кода демонстрируется разметка и код, необходимые для реализации Windows приложения ленты с помощью контекстпопупс.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: f0c739e368a26b2664b71efd4ff7cd8c3e7f8490ef7df8ccbe8ec6ace18af115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964393"
---
# <a name="contextpopup-sample"></a>Пример Контекстпопуп

в этом примере кода демонстрируется разметка и код, необходимые для реализации Windows приложения ленты с помощью контекстпопупс.

- [Использование](#usage)
  - [Создание примера](#building-the-sample)
  - [Запуск примера](#running-the-sample)
- [Поддержка](#support)
- [Минимальные требования](#minimum-requirements)
- [Связанные темы](#related-topics)

## <a name="usage"></a>Использование

примеры платформы ленты Windows можно скачать в виде автономных Microsoft Visual Studio проектов из [центра загрузки майкрософт](https://www.microsoft.com/download/details.aspx?id=9620) или установить в составе [Windows пакета средств разработки программного обеспечения (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).

- Windows пакет средств разработки программного обеспечения (SDK) (стандартный путь установки):% ProgramFiles% \\ пакеты sdk майкрософт \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ контекстпопуп

### <a name="building-the-sample"></a>Построение образца

Скачайте пример.

установите Windows SDK для Windows 7 и откройте командное окно среды сборки. В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.

Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца. В командной строке введите команду MSBUILD.

Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.

### <a name="running-the-sample"></a>Запуск примера

Чтобы запустить пример из окна командной строки среды сборки, выполните .exe файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.

Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.

## <a name="support"></a>Поддержка

на [форуме Windows ribbon](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задать вопросы, связанные с разработкой приложений ленты Windows.

## <a name="minimum-requirements"></a>Минимальные требования



| Требование | Значение |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 7<br/> Windows vista с пакетом обновления 2 (sp2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Минимальная версия сервера | Windows Server 2008 R2<br/> Windows сервер 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Пакет Windows SDK              | 7,0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Заголовочные и IDL-файлы     | уириббон. h, уириббон. idl                                                                                                                                                 |



 

> [!Note]  
> [обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows приложения ленты как Windows Vista, так и Windows Server 2008. обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows. сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , Центр обновления Windows могут определить, установлено ли необходимое обновление. если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Контекстное всплывающее окно](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





