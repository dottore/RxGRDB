use_frameworks!
workspace 'RxGRDB.xcworkspace'

def common_pods
  pod 'RxSwift', '~> 5.0'
  # pod 'GRDB.swift', '~> 4.0'
  # pod 'GRDB.swift', path: '../GRDB.swift'
  pod 'GRDB.swift', git: 'https://github.com/groue/GRDB.swift.git', branch: 'GRDB-4.1'
end

def test_pods
  pod 'RxBlocking'
end

target 'RxGRDBiOS' do
  platform :ios, '9.0'
  common_pods
end

target 'RxGRDBmacOS' do
  platform :macos, '10.10'
  common_pods
end

target 'RxGRDBiOSTests' do
  platform :ios, '9.0'
  common_pods
  test_pods
end

target 'RxGRDBmacOSTests' do
  platform :macos, '10.10'
  common_pods
  test_pods
end

target 'RxGRDBDemo' do
  project 'Documentation/RxGRDBDemo/RxGRDBDemo.xcodeproj'
  platform :ios, '9.0'
  pod 'RxDataSources'
  pod 'RxGRDB', :path => '.'
end