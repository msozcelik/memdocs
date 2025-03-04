---
author: ErikjeMS
ms.author: erikje
ms.service: microsoft-intune
ms.subservice: fundamentals
ms.topic: include
ms.date: 09/18/2023
ms.localizationpriority: high
---

### Apple

- Apple iOS 15.0 and later
- Apple iPadOS 15.0 and later
- macOS 11.0 and later

> [!NOTE]
> Intune requires iOS 14.x or later for device enrollment scenarios and app configuration delivered through Managed devices app configuration policies.
>
> For Intune app protection policies and app configuration delivered through Managed apps App configuration policies, Intune requires iOS 14.x or later.  

In the context of userless iOS/iPadOS devices, there's a difference between *supported* OS versions and *allowed* OS versions. For more information, see [Support statement for supported versus allowed iOS/iPadOS versions for user-less devices](https://techcommunity.microsoft.com/t5/intune-customer-success/support-statement-for-supported-versus-allowed-ios-ipados/ba-p/3484657).  

### Android

- Android 8.0 and later (including Samsung KNOX Standard 3.0 and higher: [requirements](https://www.samsungknox.com/en/knox-platform/supported-devices/2.4+))
- Android enterprise: [requirements](https://support.google.com/work/android/topic/9428066)
- Android open source project device: [requirements](../fundamentals/android-os-project-supported-devices.md)
[!INCLUDE [android-supported-os](android-supported-os.md)]

### Linux

- Ubuntu Desktop 22.04 LTS with a GNOME graphical desktop environment
- Ubuntu Desktop 20.04 LTS with a GNOME graphical desktop environment

> [!NOTE]
> Ubuntu Desktop already has a GNOME graphical desktop environment installed.

### Microsoft

- Windows 10/11 (Home, S, Pro, Education, Enterprise, and IoT Enterprise editions)
- Windows 10/11 Cloud PCs on Windows 365

  > [!NOTE]
  > You can continue to use Microsoft Intune to manage devices running Windows 11 the same as with Windows 10. If another article doesn't explicitly reference Windows 11, assume that feature support for Windows 10 also includes Windows 11.
  >
  > Some features may not be available on Windows 11. This article lists some [known issues](#windows-11-known-issues). As always, test your policies before broadly deploying them across your devices.

- Windows 10 LTSC 2019/2021 (Enterprise and IoT Enterprise editions)

  For more information about managing devices running Windows 10 LTSC 2019, see [What's new in Windows 10 Enterprise LTSC 2019](/windows/whats-new/ltsc/whats-new-windows-10-2019)
  
- Windows 10 version 1709 (RS3) and later, Windows 8.1 RT, PCs running Windows 8.1 (Sustaining mode)

- Windows Holographic for Business

  For more information about managing devices running Windows Holographic for Business, see [Windows Holographic for Business support](../fundamentals/windows-holographic-for-business.md).

- Surface Hub

- Windows 10 Teams (Surface Hub)

  For more information about managing devices running Windows 10 Teams, see [Manage Surface Hub with MDM](/surface-hub/manage-settings-with-mdm-for-surface-hub)

> [!NOTE]
> Not all Windows editions support all available operating system features being configured through MDM. For more information, see the [Windows configuration service provider reference docs](/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers). Each CSP highlights which Windows editions are supported.

Customers with Enterprise Management + Security (EMS) can also use [Azure Active Directory (Azure AD) to register Windows 10 devices](../enrollment/windows-enroll.md).

For guidelines on using Windows 10 virtual machines with Intune, see [Using Windows 10 virtual machines](../fundamentals/windows-10-virtual-machines.md).

> [!NOTE]
> Intune does not currently support managing UWF enabled devices. For more information, see [Unified Write Filter (UWF) feature](/windows-hardware/customize/enterprise/unified-write-filter).

### Windows 11 known issues

- Currently, you can use Intune to configure a single-app kiosk on Windows 11 devices. For more information about Windows 11 multi-app kiosk support, go to [Set up a multi-app kiosk on Windows 11 devices](/windows/configuration/lock-down-windows-11-to-specific-apps).

  For more information on dedicated kiosk devices in Intune, go to [Windows and Windows Holographic for Business device settings to run as a dedicated kiosk using Intune](../configuration/kiosk-settings.md).

- Management capabilities to deliver customized Start and Taskbar experiences are currently limited. For more information, see the following articles:

  - [Supported configuration service provider (CSP) policies for Windows 11 Start menu](/windows/configuration/supported-csp-start-menu-layout-windows)
  - [Supported configuration service provider (CSP) policies for Windows 11 taskbar](/windows/configuration/supported-csp-taskbar-windows)
  - [Windows device settings to allow or restrict features using Intune](../configuration/device-restrictions-windows-10.md)
