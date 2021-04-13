---
description: Ниже приведены часто задаваемые вопросы о разработке для компонентов платформы Tablet PC, установленных с помощью пакета SDK для Windows Vista.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Часто задаваемые вопросы (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104414321"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Часто задаваемые вопросы о разработке для платформы Tablet PC

Ниже приведены часто задаваемые вопросы о разработке для компонентов платформы Tablet PC, установленных с помощью пакета SDK для Windows Vista.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>У. Можно ли использовать интерфейсы API рукописного ввода или элементы управления на веб-странице?

A. Да. Управляемая библиотека Tablet PC поддерживает частично доверенные среды, а именно выполнение управляемых сборок с веб-страниц.

Также поддерживается развертывание в браузере приложений, использующих Windows Presentation Foundation.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>У. Нужен ли мне планшетный ПК для разработки приложений для планшетных ПК?

A. Нет, компоненты платформы Tablet PC, установленные Windows SDK, включают расширения и служебные программы, необходимые для разработки программного обеспечения для планшетных ПК на настольном или переносном компьютере. Вы можете использовать мышь или внешний планшет для рукописного ввода и рисования.

Компоненты платформы Tablet PC, установленные Windows SDK, могут быть установлены на Windows XP Professional или Windows Server 2003, но для приложений доступны менее функциональные возможности. На этих платформах приложение может составлять рукописные данные с помощью объектов [**InkCollector**](inkcollector-class.md) и [**InkOverlay**](inkoverlay-class.md) , а также тестировать и отлаживать их.

Кроме того, элементы управления [InkEdit](inkedit-control-reference.md) и [InkPicture](inkpicture-control-reference.md) могут сосуществовать рукописных данных в этих операционных системах только в том случае, если компоненты платформы tablet PC установлены из Windows SDK (или более старой версии пакета средств разработки для планшетных ПК). они не собираются в приложениях, которые перераспределяются на компьютеры, отличные от планшета, без установленных компонентов платформы.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>У. Нужно ли запускать специальную версию Windows для распознавания рукописного текста?

A. Нет. Хотя только Windows XP Tablet PC Edition и некоторые версии Windows Vista включают Распознаватели рукописного ввода, вы можете загрузить [пакет распознавателя Windows XP Tablet PC edition 2005]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) и установить его на Windows XP Professional или windows Server 2003 только в целях разработки. Вы не можете распространять распознаватели вместе с приложением.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>У. В чем разница между технологиями Windows Vista и Tablet PC?

A. Планшетные ПК работают под управлением операционной системы Windows Vista, в которой реализованы все функции Windows Vista и дополнительные функции, характерные для планшетных ПК. Эти функции технологии Tablet PC позволяют пользователям запускать приложения Windows и Windows с помощью пера, заметок документов и создания рукописных документов с помощью цифрового рукописного ввода. Технология для планшетных ПК доступна в большинстве версий Windows Vista, и если на компьютере доступно оборудование Tablet PC, функции просто работают.

Для более ранних версий операционных систем Windows, которые изначально не поддерживают рукописный ввод, можно повторно распространять и использовать элементы управления рукописным вводом Tablet PC для просмотра рукописного ввода на планшетном ПК.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>У. В чем разница между Windows XP Tablet PC Edition и Windows XP Tablet PC Edition 2005?

A. Windows XP Tablet PC Edition 2005 — это обновленная версия Windows XP Tablet PC Edition.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>У. Разделы справки изменить приложение для запуска на планшетном ПК?

A. Приложения Microsoft Windows, работающие на настольном компьютере или ноутбуке Windows XP с сравнимым оборудованием, могут работать на планшетном ПК без изменений.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>У. Я понимаю, что мне не нужно вносить какие-либо изменения в приложение, но его трудно использовать с помощью пера и речи. Что можно сделать для оптимизации моего приложения для планшетных ПК?

A. API-интерфейсы и элементы управления рукописным вводом компонентов платформы Tablet PC можно использовать для создания пользовательских интерфейсов, которые лучше подходят для рукописного ввода и распознавания текста. Дополнительные сведения о конкретных способах улучшения приложения см. в статье [Руководство пользователя по работе с мобильными ПК для разработчиков](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>У. Какие языки программирования поддерживает планшет?

A. Технология планшетных ПК в Windows Vista поддерживает COM (C++) и управляемые библиотеки (набор языков Visual Studio .NET).

Технология Tablet PC также поддерживает Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>У. У меня есть пример кода, демонстрирующий возможности платформы планшетов?

A. Да, пример кода для COM и выбранных управляемых языков входит в состав компонентов платформы Tablet PC, установленных с помощью пакета SDK для платформы Windows.

Доступные примеры приложений см. в следующих статьях:

- [Примеры для мобильных и планшетных ПК](mobile-pc-and-tablet-pc-samples.md)
- [Примеры цифровых рукописных фрагментов, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ образцы \\ TabletPC

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>У. Каков базовый уровень оборудования планшета, для которого мне нужно разработать?

A. В общем случае следует разработать систему, совместимую с Windows Vista без унаследованных систем.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>У. Какие рекомендации по пользовательскому интерфейсу можно предоставить для приложений планшета?

A. Проблемы с ориентацией раскрывающегося меню на экран или дигитайзер фокусировки описаны в руководстве по работе с мобильными [ПК для разработчиков](/previous-versions//dd356056(v=vs.85)) в разделе Windows SDK.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>У. Включены ли жесты рукописного ввода системного уровня для часто используемых клавиш? Можно ли создать собственные жесты для использования при запуске приложения или его фокусе?

A. Да, мы включаем набор жестов для событий мыши. Кроме того, можно создавать жесты для использования в приложении. Дополнительные сведения о жестах см. [в разделе Использование жестов](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>У. Как определить, работает ли приложение на планшете?

A. Используйте Жетсистемметриксапи Windows и передайте \_ значение индекса в SM TABLETPC. SM \_ TABLETPC определен в файле WinUser. h. Значение SM \_ TABLETPC равно 86.

Для разработки веб-приложений необходимо прочитать \_ \_ переменную среды строки агента пользователя. Вы можете получить доступ к этой коллекции Request. ServerVariables.

Дополнительные сведения об использовании Жетсистемметрикс на планшетных ПК под управлением Windows Vista или Windows XP Tablet PC Edition см. в статье [Определение того, является ли компьютер планшетным ПК](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>У. Как определить, доступны ли компоненты платформы планшета?

A. Некоторые части платформы Tablet PC могут быть установлены в операционных системах Windows XP Professional, Windows Server 2003 и Windows 2000, не являющихся планшетными.

Правильный способ определить, установлен ли компонент API, — попытаться создать экземпляр объекта или элемента управления и проверить, что он существует, прежде чем пытаться его использовать.

Например, чтобы определить, доступен ли объект [**InkCollector**](inkcollector-class.md) , попытайтесь создать его с помощью [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>У. Разделы справки запустить службу ввода планшетов в SKU сервера?

A. Таблетинпутсервице не запускается автоматически в SKU сервера при установке клиентского пакета. Клиентский пакет устанавливает все компоненты платформы, чтобы любые клиентские приложения для планшета также могли работать на сервере. Служба ввода планшетов прослушивает уведомление PnP о подключении внешнего дигитайзера. Чтобы включить службу ввода планшета на сервере, используйте программу настройки системы.

В меню **Пуск** выберите команду **выполнить**. Введите "MSCONFIG" и нажмите клавишу ВВОД. Перейдите на вкладку **службы** , найдите службы с именем "служба ввода HID", установите флажок рядом с ней и нажмите кнопку **Применить**. Закройте программу.

## <a name="q-more-faqs-and-other-resources"></a>У. Другие часто задаваемые вопросы и другие ресурсы

- [Центр разработки Майкрософт](https://developer.microsoft.com)
- [Справочник по основным ПК на платформе Tablet PC](./core-reference---tablet-pc-com-library.md)